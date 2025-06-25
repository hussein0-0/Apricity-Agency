<script>
  import ServicesDetails from "../shared/ServicesDetails.svelte";
  import { gsap } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  import TextPlugin from "gsap/TextPlugin";
  import { onMount } from "svelte";

  onMount(() => {
    gsap.from('.services',{
      scrollTrigger: {
        trigger: ".services",
        start: "top 40%",
        toggleActions: "play none none none",
      },
      duration:1.5,
      opacity:0,
      x:'60%',
      ease: 'power2.inOut',
      stagger: 0.2
    })
  });
</script>

<section id="Services">
  <div class="wave-container">
    <svg class="wave" viewBox="0 0 1440 250" preserveAspectRatio="none">
          <path fill="rgb(6, 26, 50)" fill-opacity="1" 
          d="M0,128L48,144C96,160,192,192,288,202.7C384,213,480,203,576,176C672,149,768,107,864,80C960,53,1056,43,1152,53.3C1248,64,1344,96,1392,112L1440,128L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z">
          </path>
    </svg>
  </div>
    <div class="services">
    <h2>Services</h2>
  </div>
</section>

<style>

section {
  background-color: #ffffff;
  color: rgb(11, 27, 49);
  position: relative;
}

.wave-container {
  margin: -0.2vw 0vw;
  position: absolute;
  top:0;
  left: 0;
  width: 100%;
  overflow-x: hidden;
}

.services{
  margin-bottom: -0.2vw;
  display: flex;
  justify-content: flex-end;
  padding: 8vw 5vw;
}

.services h2 {
  font-size: 10.4vw;
  font-weight: 1000;
  font-family: "Heading";
  position: absolute;
  z-index: 1;
}

/* Tablet styles */
@media (max-width: 1024px) {
  .services{
    padding: 8vw 3vw;
  }
  .services h2{
    font-size: 11vw;
  }
}

/* Mobile styles */
@media (max-width: 480px) {
    section{  
      margin-bottom: 0;
    }
    .services{
      padding: 9vw 6vw ;
    }
    .services h2{
      font-size: 10vw;
    }
}
</style>