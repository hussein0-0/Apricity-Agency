<script>
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/all";
  import { onMount } from "svelte";
  import * as THREE from "three";
  import { GLTFLoader } from "three/examples/jsm/loaders/GLTFLoader.js";

  let container;
  let why, us;

  let baseYWhy_y = 0,
    baseYUs_y = 0;
  let baseYWhy_z = 0,
    baseYUs_z = 0;

  const floatAmplitude = 0.01; //! Hover height
  const floatSpeed = 2; //! Speed of bobbing
  const waveAmplitude = 0.02; // Rotation in radians (~11 degrees)
  const waveSpeed = 1.2;

  let clock = new THREE.Clock();

  gsap.registerPlugin(ScrollTrigger);

  onMount(() => {
    const scene = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(
      75,
      container.clientWidth / container.clientHeight,
      0.1,
      1000
    );
    // camera.position.set(1.25,0,0);
    const renderer = new THREE.WebGLRenderer({ antialias: true });
    renderer.setSize(container.clientWidth, container.clientHeight);
    renderer.setClearColor(0x000000, 0);
    container.appendChild(renderer.domElement);

    const loader = new GLTFLoader();

    loader.load("/why.glb", (gltf) => {
      why = gltf.scene;
      scene.add(why);
    });

    loader.load("/us.glb", (gltf) => {
      us = gltf.scene;
      scene.add(us);
    });

    const light = new THREE.AmbientLight(0xffffff, 4);
    scene.add(light);

    camera.position.z = 1;

    const animate = () => {
      requestAnimationFrame(animate);

      const time = clock.getElapsedTime();

      if (why) {
        why.position.y =
          baseYWhy_y + Math.sin(time * floatSpeed) * floatAmplitude;

        why.rotation.y = Math.sin(time * waveSpeed) * waveAmplitude;
      }

      if (us) {
        us.position.y =
          baseYUs_y +
          Math.sin(time * floatSpeed + Math.PI / 2) * floatAmplitude;

        us.rotation.y =
          Math.cos(time * waveSpeed + Math.PI / 2) * waveAmplitude;
      }

      renderer.render(scene, camera);
    };

    animate();

    const handleResize = () => {
      camera.aspect = container.clientWidth / container.clientHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(container.clientWidth, container.clientHeight);
    };

    window.addEventListener("resize", handleResize);

    gsap.from(".viewer", {
      scrollTrigger: {
        trigger: ".viewer",
        start: "top 70%",
        end: "bottom 45",
        toggleActions: "play reverse play reverse",
      },
      duration: 2.5,
      opacity: 0,
      x: -100,
    });

    return () => {
      window.removeEventListener("resize", handleResize);
    };
  });
</script>

<div bind:this={container} class="viewer"></div>

<style>
  .viewer {
    position: absolute;
    right: 0;
    width: 70%;
    height: 50%;
    background: transparent;
    z-index: 2;
  }
</style>
