<script>
  import AgencyName from "../Components/AgencyName.svelte";
  import NavBar from "../Components/NavBar.svelte";
  import About from "../Components/About.svelte";
  import SevricesTitle from "../Components/SevricesTitle.svelte";
  import ServicesContent from "../Components/ServicesContent.svelte";
  import WhyUs from "../Components/WhyUs.svelte";
  import OurTeamTitle from "../Components/OurTeamTitle.svelte";
  import Card from "../Components/Card.svelte";
  import Footer from "../Components/Footer.svelte";
  import ApricityName from "../Components/ApricityName.svelte";
  import ShowModel from "../Components/showModel.svelte";
  import {onMount} from "svelte"
  let loading = true;
  onMount(() => {
    setTimeout(() => {loading = false;}, 1500);
  });
</script>

{#if loading}
  <div class="loading">
    <div class="spinner"></div>
    <p>Loading...</p>
  </div>
{:else}
<main>
  <title>Apricity Agency</title>
  <NavBar />
  <AgencyName />
  <About />
  <SevricesTitle />
  <ServicesContent />
  <WhyUs />
  <OurTeamTitle />
  <Card />
  <Footer />
</main>
{/if}

<style>
  main {
    background-color: rgb(6, 26, 50);
    overflow-x: hidden;
    margin: 0;
    padding: 0;
  }
  @font-face {
    font-family: "Title";
    src: url(../fonts/COPRGTL.TTF) format("truetype");
  }
  @font-face {
    font-family: "Heading";
    src: url(../fonts/FontsFree-Net-Montserrat-Black-1.ttf) format("truetype");
  }
  @font-face {
    font-family: "Nunito_Black";
    src: url(../fonts/FontsFree-Net-Nunito-Black.ttf) format("truetype");
  }
  @font-face {
    font-family: "Poppins_Regular";
    src: url(../fonts/FontsFree-Net-Poppins-Regular.ttf) format("truetype");
  }
  @font-face {
    font-family: "Nunito_Bold";
    src: url(../fonts/FontsFree-Net-Nunito-Bold.ttf) format("truetype");
  }
  @font-face {
    font-family: "Nunito_SemiBold";
    src: url(../fonts/FontsFree-Net-Nunito-SemiBold.ttf) format("truetype");
  }
  @font-face {
    font-family: "Nunito_Regular";
    src: url(../fonts/FontsFree-Net-Nunito-Regular.ttf) format("truetype");
  }
  
  .loading {
    position: fixed;
    inset: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: rgb(6, 26, 50);
    color: #e2a243;
    font-family: "Nunito_SemiBold";
    font-size: 1.2rem;
    z-index: 9999;
  }

  .spinner {
    width: 5rem;
    height: 5rem;
    border: 0.4rem solid rgba(255, 255, 255, 0.2);
    border-top-color: #e2a243;
    border-radius: 50%;
    animation: spin 1s linear infinite;
    margin-bottom: 1.5rem;
  }

  @keyframes spin {
    to {
      transform: rotate(360deg);
    }
  }
</style>
