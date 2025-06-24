<script>
  import Form from "./Form.svelte";

  let showForm = false;
  let mobileMenuOpen = false;
  
  function ClickHandeler(){
    showForm = !showForm;
    console.log("clicked")
  }
  
  function toggleMobileMenu() {
    mobileMenuOpen = !mobileMenuOpen;
  }
</script>

<Form {showForm} on:click={ClickHandeler}/>
<main>
    <header id="Home">
        <nav>
            <div class="logo">APRICITY</div>
            <button class="mobile-menu-toggle" on:click={toggleMobileMenu}>
                <span>.</span>
                <span></span>
                <span></span>
            </button>
            <ul class="nav_items" class:active={mobileMenuOpen}>
                <button class="close" class:active={mobileMenuOpen} on:click={toggleMobileMenu}>X</button>
                <li><a href="#Home" on:click={() => mobileMenuOpen = false}>Home</a></li>
                <li><a href="#About" on:click={() => mobileMenuOpen = false}>About us</a></li>
                <li><a href="#Services" on:click={() => mobileMenuOpen = false}>Services</a></li>
                <li><a href="#WhyUs" on:click={() => mobileMenuOpen = false}>Why us</a></li>
                <li><a href="#Team" on:click={() => mobileMenuOpen = false}>Team</a></li>
            </ul>
            <button on:click={ClickHandeler}>Become a client?</button>
        </nav>
    </header>
</main>

<style>
header{
    background-color: rgb(6, 26, 50);
}

nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 3vw 5vw 5vw 6vw;
    position: relative;
}

.logo{
    color: transparent;
    text-shadow: 0.15vw 0.17vw 0.6vw rgb(0, 0, 0, 0.8), 0 0 0 #E2A243;
    font-size: 2.2vw;
    font-weight: bold;
    font-family: "Title";
    letter-spacing: 0.05em;
}

.mobile-menu-toggle {
    display: none;
}

.close{
    display: none;
}

.nav_items{
    list-style:none;
    display: flex;
    align-items: center;
}

.nav_items li{
    display: inline-block;
    padding: 0vw 3.2vw;
    font-size: 1.3vw;
}

.nav_items a{
    font-family: "Nunito_Regular";
    color: white;
    text-decoration: none;
    letter-spacing: 0.1vw;  
}

button{
    font-family: "Nunito_SemiBold";
    cursor: pointer;
    font-size: 1vw;
    color:white;
    background: #c88d34;
    border: none;
    border-radius: 2vw;
    padding: 1em 1.6em;
}

/* Tablet styles */
@media (max-width: 1024px) {
    nav{
        padding: 3vw 4vw;
    }
    .logo{
        font-size: 2.2vw;
        padding-right: 1vw;
        
    }
    .nav_items li{
        font-size: 1.6vw;
    }
    button{
        font-size: 1.5vw;
        padding: 1.4vw 1vw;
        border-radius: 3vw;
    }
}

/* Mobile styles */
@media (max-width: 480px) {
    main{
        margin-bottom: 0;
    }

    nav {
        padding: 4vw 3vw;
        flex-wrap: 
        wrap;
    }
    .mobile-menu-toggle span {
        font-size: 0;
        width: 6vw;
        height: 0.8vw;
        background-color: #E2A243;
        margin: 0.6vw 0 0 0;
    }

    .mobile-menu-toggle {
        display: flex;
        flex-direction: column;
        cursor: pointer;
        background-color: transparent;
    }
    
    .nav_items {
        position: absolute;
        top: 0;
        right: -100%;
        width: 50%;
        height: 50vh;
        background-color: rgb(6, 26, 50);
        flex-direction: column;
        justify-content: center;
        align-items: center;
        border: 1px solid white;
        transition: 0.4s ease-in-out;
        z-index: 10;
    }

    .nav_items.active {
        right: 0;
    }

    .nav_items li {
        padding: 4vw 0;
        font-size: 4.8vw;
    }

    button {
        display: none;
    }

    .logo {
        text-shadow: 0.6vw 0.5vw 1.6vw rgb(0, 0, 0, 0.8), 0 0 0 #E2A243;
        font-size: 5vw;
    }

    .close{
        display: flex;
        position: absolute;
        right: 0;
        top: 0;
        font-size: 2vh;
        background-color: transparent;
        border: none;
    }    
}
</style>