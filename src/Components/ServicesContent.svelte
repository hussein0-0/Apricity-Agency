<script>
  import ServicesDetails from "../shared/ServicesDetails.svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  import TextPlugin from "gsap/TextPlugin";
  import { onMount } from "svelte";
  import ShowModel from "./showModel.svelte";

  // onMount(() => {
  //   gsap.from()
  // });
</script>


<section>
  <ServicesDetails
    Title="Website UI/UX Design"
    Disc="We craft intuitive and visually stunning interfaces that focus on clarity, usability, and brand identity."
  />
  <ServicesDetails
    Title="App Design & Development"
    Disc="Custom Android & iOS applications built for performance, aesthetics, and seamless user experience."
  />
  <ServicesDetails
    Title="Frontend Development (React & Svelte)"
    Disc="Modern, responsive, and fast-loading frontend solutions using powerful frameworks like React and Svelte."
  />
  <ServicesDetails
    Title="Backend Development"
    Disc="Robust and scalable backend systems tailored to your business logic, with seamless API integration."
  />
  <ServicesDetails
    Title="Educational Tech Content"
    Disc="We share simplified tech tutorials, coding tips, and curated programming resources for learners of all levels."
  />
  <ShowModel />
</section>

<style>
  section {
    background-color: #ffffff;
    padding: 2vw 0vw 15vw 0vw;
    overflow: hidden;
    margin: 0;
    padding-top: 7vw;
  }

  /* Tablet styles */
  @media (max-width: 1024px) {
    section {
      padding-bottom: 10vw;
    }
  }

  /* Mobile styles */
  @media (max-width: 480px) {
    section {
      padding: 6vw 0vw 16vw 0vw;
    }
  }
</style>
