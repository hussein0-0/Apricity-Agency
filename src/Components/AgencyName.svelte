<script>
  import { gsap } from "gsap";
  import { onMount } from "svelte";
  import { TextPlugin } from "gsap/TextPlugin";
  import ApricityName from "./ApricityName.svelte";

  gsap.registerPlugin(TextPlugin);
  let wordEl;

  onMount(() => {
    let index = 0;
    let words = ["Success", "Innovation", "Growth", "Vision", "Impact"];

    function changeWord() {
      gsap.to(wordEl, {
        duration: 1,
        text: words[index],
        ease: "power2.inOut",
        onComplete: () => {
          index = (index + 1) % words.length;
          setTimeout(changeWord, 1000); // timer to wait before changing again uwu
        },
      });
    }
    changeWord();
    
    gsap.to('#desc-text',{
      duration:1,
      opacity:1,
      ease: 'power2.inOut'
    })
  });
</script>

<div class="name">
  <ApricityName/>
  <p id="desc-text">
    From Idea To <span>Creativity</span>,<br />
    Reaching the Summit of
    <span class="word-container">
      <span bind:this={wordEl} id="word" style="color:#E2A243;"></span></span
    >.
  </p>
</div>

<style>
  .name {
    background-color: rgb(6, 26, 50);
    text-align: center;
    padding: 18vh 0vw;
  }

  .name p {
    opacity: 0;
    font-size: 2vw;
    color: white;
    font-family: "Nunito_Regular";
    margin-top: 9vw;
  }

  .word-container {
    display: inline-block;
    overflow: hidden;
    vertical-align: bottom;
    position: relative;
  }

  #word {
    display: inline-block;
    color: #e2a243;
    position: relative;
  }

  /* Tablet styles */
  @media (max-width: 1024px) {
    .name h2 {
      font-size: 8vw;
    }
    .name p {
      font-size: 3.4vw;
      margin-top: 15vw;
    }
  }

  /* Mobile styles */
  @media (max-width: 480px) {
    .name {
      margin: -0.2vw 0vw;
      padding: 25vw 0vw 20vw 0vw;
    }
    .name h2 {
      text-shadow:
        0.6vw 0.5vw 1.6vw rgb(0, 0, 0, 0.8),
        0 0 0 #e2a243;
      font-size: 14vw;
    }
    .name p {
      padding: 5vw 0vw;
      font-size: 4.6vw;
      margin-top: 15vw;
    }
  }
</style>
