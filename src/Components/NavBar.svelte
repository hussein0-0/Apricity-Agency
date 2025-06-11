<main>
    <header id="Home">
        <nav>
            <div class="logo">APRICITY</div>
            <ul class="nav_items">
                <li><a href="#Home">Home</a></li>
                <li><a href="#About">About us</a></li>
                <li><a href="#Services">Services</a></li>
                <li><a href="#WhyUs">Why us</a></li>
                <li><a href="#Team">Team</a></li>
            </ul>
            <button>Become a client?</button>
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
    padding: 2rem 5rem 5rem 6rem;
}

.logo{
    color: transparent;
     text-shadow: 10px -4px 15px rgb(0, 0, 0, 0.8), 0 0 0 #E2A243;
    font-size: 2rem;
    font-weight: bold;
    font-family: "Title";
    letter-spacing: 0.05em;
}

.nav_items{
    list-style:none;
}

.nav_items li{
    display: inline-block;
    padding: 0rem 3rem;
    font-size: 1.2rem;
}

.nav_items a{
    font-family: "Nunito_Regular";
    color: white;
    text-decoration: none;
    letter-spacing: 1px;  
}

button{
    font-family: "Nunito_SemiBold";
    cursor: pointer;
    font-size: 1rem;
    color:white;
    background: #c88d34;
    border: none;
    border-radius: 2rem;
    padding: 1em 1.6em;
}

</style>