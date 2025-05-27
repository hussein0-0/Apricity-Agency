
<main>
    <header>
        <nav>
            <div class="logo">APRICITY</div>
            <ul class="nav_items">
                <li><a href="">Home</a></li>
                <li><a href="">About us</a></li>
                <li><a href="">Protfolio</a></li>
                <li><a href="">Services</a></li>
                <li><a href="">Team</a></li>
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
    padding: 2rem 5rem 5rem 3rem;
}

.logo{
    color:rgb(251, 176, 59 , 0.8) ;
    font-size: 2.5rem;
    font-weight: bold;
    font-family: "logo";
    letter-spacing: 0.05em;
    text-shadow: 2px 2px 13px #000000;
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
    color: white;
    text-decoration: none;
    font-family: nunito;
    letter-spacing: 1px;
    
}

button{
    cursor: pointer;
    font-size: 1rem;
    color:white;
    background: rgb(251, 176, 59,0.8);
    border: none;
    border-radius: 2rem;
    padding: 1.1em 1.6em;
}

</style>