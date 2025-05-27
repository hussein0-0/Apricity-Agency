<script>
  import AgencyName from "../Components/AgencyName.svelte";
  import NavBar from "../Components/NavBar.svelte";
  import About from "../Components/About.svelte";
  import SevricesTitle from "../Components/SevricesTitle.svelte";
  import ServicesContent from "../Components/ServicesContent.svelte";
  import WhyUs from "../Components/WhyUs.svelte";


</script>

<main>
  <link href="https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200..1000;1,200..1000&display=swap" rel="stylesheet">
    <title>Apricity Agency</title>
    <NavBar/>
    <AgencyName/>
    <About/>
    <SevricesTitle/>
    <ServicesContent/>
    <WhyUs/>
</main>

<style>
@font-face{
  font-family: "logo";
  src: url(../fonts/Copperplate-Gothic-Std-29-AB.ttf) format('truetype');
}
@font-face{
  font-family: "Heading";
  src: url(../fonts/FontsFree-Net-Montserrat-Black-1.ttf) format('truetype');
}
</style>