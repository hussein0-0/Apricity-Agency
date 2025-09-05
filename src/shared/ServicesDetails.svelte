<script>
  import ServicesDetails from "../shared/ServicesDetails.svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  import { onMount } from "svelte";

  gsap.registerPlugin(ScrollTrigger);

  export let Title;
  export let Disc;

  let serEl;

onMount(() => {
  const tl = gsap.timeline({
    scrollTrigger: {
      trigger: serEl,
      start: "top 95%",
      end: "bottom 75%",
      scrub: 0.6,
    }
  });

  tl.to(serEl.querySelector(".title"), {
    x: "-19vw",
    ease: "power2.out",
  }, 0)
  .to(serEl.querySelector(".disc"), {
    x: "19vw",
    ease: "power2.out",
  }, 0);
});

</script>

<div bind:this={serEl} class="container">
  <div class="title">
    <p><img src="src/Assets/icons8-bulb-384.png" alt="" /> {Title}</p>
  </div>
  <div class="disc"><p>{Disc}</p></div>
</div>

<style>
  .container {
    position: relative;
    padding: 3vw 0vw;
    margin: 0vw 3.2vw;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0;
    flex-wrap: nowrap;
    overflow: visible;
  }

  .title {
    position: relative;
    display: inline-block;
    color: #ffffff;
    border: 0.3vw solid rgb(11, 27, 49);
    border-radius: 5.2vw;
    background-color: rgb(11, 27, 49);
    width: 51vw;
    height: 12.55vw;
    display: flex;
    align-items: center;
    z-index: 2;
    margin-right: -24vw;
  }

  .disc {
    position: relative;
    display: inline-block;
    right: 0;
    color: rgb(11, 27, 49);
    border: 0.3vw solid rgb(11, 27, 49);
    border-radius: 5.2vw;
    background-color: rgb(11, 27, 49, 0.1);
    width: 51vw;
    height: 12.55vw;
    display: flex;
    align-items: center;
    text-align: start;
    z-index: 1;
    margin-left: -24vw;
  }

  .title p {
    font-family: "Nunito_Bold";
    text-align: left;
    font-size: 2.3vw;
    font-weight: bold;
    padding-left: 2.1vw;
  }

  .disc p {
    font-family: "Poppins_Regular";
    font-size: 1.7vw;
    font-weight: 500;
    padding: 0vw 3vw 0vw 11.2vw;
  }
  img {
    width: 2.3vw;
    margin: 0vw 1vw;
  }

  .title, .disc {
  will-change: transform;
}


  /* Tablet styles */
  @media (max-width: 1024px) {
    .container {
      padding: 3vw 0vw;
      margin: 2vw 2vw;
    }
    .title,
    .disc {
      width: 52.5vw;
      height: 15vw;
    }
    .title p {
      font-size: 2.4vw;
      padding-left: 1.3vw;
    }
    .disc p {
      font-size: 1.85vw;
      padding: 0vw 3vw 0vw 13vw;
    }
    img {
      width: 2.5vw;
      margin: 0vw 0.8vw;
    }
  }

  /* Mobile styles */
  @media (max-width: 480px) {
    .container {
      display: flex;
      flex-wrap: wrap;
      margin-top: 7vw;
      padding: 0;
    }
    .title {
      position: relative;
      width: 100%;
      margin: 0 0 -9vw 0;
      height: 22vw;
      border-radius: 4vw;
    }
    .disc {
      margin: 0;
      position: relative;
      width: 100%;
      height: 22vw;
      border-radius: 4vw;
    }
    .title p {
      font-size: 4.5vw;
    }
    .disc p {
      padding: 8vw 2vw 0vw 3vw;
      font-size: 3vw;
    }
    img {
      width: 4.3vw;
      margin: 0vw 1.2vw;
    }
  }
</style>
