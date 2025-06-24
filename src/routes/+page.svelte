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
</script>

<main>
    <title>Apricity Agency</title>
    <NavBar/>
    <AgencyName/>
    <About/>
    <SevricesTitle/>
    <ServicesContent/>
    <WhyUs/>
    <OurTeamTitle/>
    <Card/>
    <Footer/>
</main>

<style>
  main{
    background-color: rgb(6, 26, 50);
    overflow-x: hidden;
    margin: 0;
    padding: 0;
  }
@font-face{
  font-family: "Title";
  src: url(../fonts/COPRGTL.TTF) format('truetype');
}
@font-face{
  font-family: "Heading";
  src: url(../fonts/FontsFree-Net-Montserrat-Black-1.ttf) format('truetype');
}
@font-face{
  font-family: "Nunito_Black";
  src: url(../fonts/FontsFree-Net-Nunito-Black.ttf) format('truetype');
}
@font-face{
  font-family: "Poppins_Regular";
  src: url(../fonts/FontsFree-Net-Poppins-Regular.ttf) format('truetype');
}
@font-face{
  font-family: "Nunito_Bold";
  src: url(../fonts/FontsFree-Net-Nunito-Bold.ttf) format('truetype');
}
@font-face{
  font-family: "Nunito_SemiBold";
  src: url(../fonts/FontsFree-Net-Nunito-SemiBold.ttf) format('truetype');
}
@font-face{
  font-family: "Nunito_Regular";
  src: url(../fonts/FontsFree-Net-Nunito-Regular.ttf) format('truetype');
}
</style>