<script>
    import {gsap} from 'gsap';
    import { onMount } from 'svelte';
  import Form from "./Form.svelte";

  let showForm = false;
  let mobileMenuOpen = false;

  function ClickHandeler() {
    showForm = !showForm;
    console.log("clicked");
  }

  function toggleMobileMenu() {
    mobileMenuOpen = !mobileMenuOpen;
  }

  onMount(()=>{
    gsap.from('#Home',{
        duration:1,
        ease:'power2.inOut',
        x:-100
    });

    gsap.to('#Home',{
        duration:1,
        opacity:1,
        ease: 'power2.inOut'
    })

});

</script>

<Form {showForm} on:click={ClickHandeler} />
  <header id="Home">
    <nav>
      <div class="logo"><img src="src/Assets/Apricity Logo @4x.png" alt=""></div>
      <button class="mobile-menu-toggle" on:click={toggleMobileMenu}>
        <span>.</span>
        <span></span>
        <span></span>
      </button>
      <ul class="nav_items" class:active={mobileMenuOpen}>
        <button
          class="close"
          class:active={mobileMenuOpen}
          on:click={toggleMobileMenu}><img src="src/Assets/icons8-left-96.png" alt=""></button
        >
        <li>
          <a href="#Home" on:click={() => (mobileMenuOpen = false)}>Home</a>
        </li>
        <li>
          <a href="#About" on:click={() => (mobileMenuOpen = false)}>About us</a
          >
        </li>
        <li>
          <a href="#Services" on:click={() => (mobileMenuOpen = false)}
            >Services</a
          >
        </li>
        <li>
          <a href="#WhyUs" on:click={() => (mobileMenuOpen = false)}>Why us</a>
        </li>
        <li>
          <a href="#Team" on:click={() => (mobileMenuOpen = false)}>Team</a>
        </li>
      </ul>
      <button on:click={ClickHandeler}>Become a client?</button>
    </nav>
  </header>

<style>
  header {
    background-color: rgb(6, 26, 50);
  }

  #Home{
    opacity: 0;
  }
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 3vw 5vw 5vw 6vw;
    position: relative;
  }

  .logo img{
    width: 6vw;
  }

  .mobile-menu-toggle {
    display: none;
  }

  .close {
    display: none;
  }

  .nav_items {
    list-style: none;
    display: flex;
    align-items: center;
  }

  .nav_items li {
    display: inline-block;
    padding: 0vw 3.2vw;
    font-size: 1.3vw;
  }

  .nav_items a {
    font-family: "Nunito_Regular";
    color: white;
    text-decoration: none;
    letter-spacing: 0.1vw;
    position: relative;
    padding-bottom: 0.2vw;
  }

  button {
    font-family: "Nunito_SemiBold";
    cursor: pointer;
    font-size: 1vw;
    color: white;
    background: #c88d34;
    border: none;
    border-radius: 2vw;
    padding: 1em 1.6em;
  }

  .nav_items li a::after {
    content: "";
    position: absolute;
    width: 0;
    height: 2px;
    left: 0;
    bottom: 0;
    background-color: #e2a243;
    transition: width 0.3s ease;
  }

  .nav_items li a:hover::after {
    width: 100%;
  }

  /* Tablet styles */
  @media (max-width: 1024px) {
    nav {
      padding: 3vw 4vw;
    }
    .nav_items li {
      font-size: 1.6vw;
    }
    button {
      font-size: 1.5vw;
      padding: 1.4vw 1vw;
      border-radius: 3vw;
    }
  }

  /* Mobile styles */
  @media (max-width: 480px) {
    header{
      position: fixed;
      width: 100%;
    }
    nav {
      padding: 4vw 3vw;
      flex-wrap: wrap;
      z-index: 1001;
    }
    .mobile-menu-toggle span {
      font-size: 0;
      width: 6vw;
      height: 0.3vw;
      background-color: #e2a243;
      margin: 0.16rem 0;
      padding: 0.2vw;
    }

    .mobile-menu-toggle {
      padding: 1.5vw 2vw 1.5vw 5vw;
      border: 1px solid #e2a243;
      border-radius: 1vw;
      border-bottom-right-radius: 2vw;
      position: absolute;
      top: 6rem;
      left: -2vw;
      display: flex;
      flex-direction: column;
      cursor: pointer;
      background-color: transparent;
    }

    .nav_items {
      padding: 7rem 0 0 2rem;
      position: fixed;
      top: 0rem;
      left: -100%;
      width: 60%;
      height: 100vh;
      background-color: rgb(0, 0, 0 , 0.1);
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      border: 1px solid white;
      transition: 0.4s ease-in-out;
      z-index: 1000;
      backdrop-filter: blur(1rem);
      overflow-y: auto;
    }

    .nav_items.active {
      left: 0;
    }

    .nav_items li {
      padding: 4vw 0;
      font-size: 4.8vw;
    }

    button {
      font-size: 3.2vw;
      padding: 2.5vw 2.5vw;
      border-radius: 5vw; 
    }

    .logo img{
      width: 12vw;
    }

    .close {
      display: flex;
      position: absolute;
      left: 0.3rem;
      top: 2rem;
      background-color: transparent;
      border: none;
    }
    .close img{
      width: 8vw;
      mix-blend-mode: color-burn;
    }
  }
</style>
