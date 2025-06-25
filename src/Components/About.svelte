<script>
  import { onMount } from "svelte";
  import { gsap } from "gsap";
  import ScrollTrigger from "gsap/ScrollTrigger";
  import TextPlugin from "gsap/TextPlugin";
  import SplitType from "split-type";

  gsap.registerPlugin(ScrollTrigger, TextPlugin);

  let container;

  onMount(() => {
    const paragraph = container.querySelectorAll("p");
    const split = new SplitType(paragraph, { types: "lines" });

    gsap.from(split.lines, {
      scrollTrigger: {
        trigger: container,
        start: "top 40%",
        toggleActions: "play none none none",
      },
      opacity: 0,
      y: "50%",
      duration: 1.5,
      ease: "power4.out",
      stagger: 0.2,
    });

    const about = new SplitType('.about-title', {types: 'lines'});
    gsap.from(about.lines,{
      scrollTrigger: {
        trigger: container,
        start: "top 80%",
        toggleActions: "play none none none",
      },
      opacity: 0,
      y: '50%',
      duration:2,
      ease: 'power2.inOut',
      stagger: 0.2
    });

});
</script>

<section id="About">
  <h2 class="about-title">About</h2>
  <div bind:this={container} class="content">
    <p class="space">
      We are a passionate tech team brought together by a shared belief in
      innovation and purposeful design. <br />
      Our agency is built on
      <span class="highlight">creativity, dedication, and responsibility.</span
      ><br />
      we deliver professional, fast, and reliable digital services with a unique
      touch.
    </p>
    <p>
      With expertise in UI/UX design, frontend development (React & Svelte), and
      backend architecture, we turn ideas into digital experiences that are
      smooth, scalable, and user-focused. <br />
      We're not just building websites....
      <span class="highlight">We're building journeys.</span>
    </p>
  </div>
</section>

<style>
  .about-title {
    writing-mode: vertical-rl;
    font-size: 10vw;
    font-family: "Heading";
    margin: 0vw 8vw 0vw 7vw;
  }

  section {
    background-color: rgb(6, 26, 50);
    color: white;
    display: flex;
    padding: 3.3vw;
    padding-bottom: 0vw;
  }

  .content {
    padding-top: 1vw;
    font-size: 2vw;
    padding-right: 8.1vw;
    font-family: "Nunito_Regular";
    line-height: 2.7vw;
  }

  .space {
    margin-bottom: 6.2vw;
  }

  .highlight {
    color: #e2a243;
  }

  /* Tablet styles */
  @media (max-width: 1024px) {
    .about-title {
      font-size: 15vw;
      margin: 0vw 8vw 0vw 3vw;
    }

    .content {
      padding-top: 2vw;
      font-size: 2.5vw;
      padding-right: 5vw;
      line-height: 3.3vw;
    }
  }

  /* Mobile styles */
  @media (max-width: 480px) {
    section {
      flex-direction: column;
      text-align: center;
      margin-bottom: -0.6vw;
      flex-direction: column;
      text-align: left;
      padding: 9vw 12vw;
    }
    .about-title {
      writing-mode: horizontal-tb;
      margin: 0;
      font-size: 12vw;
      margin-bottom: 9vw;
    }
    .content {
      font-size: 4.4vw;
      line-height: 7vw;
    }
    .space {
      margin-bottom: 10vw;
    }
  }
</style>
