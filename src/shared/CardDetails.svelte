<script>
    export let name;
    export let job;
    export let Insta_User;
    export let GitHub_User;
    export let LinkedIn_User;
    export let GitHub_Url;
    export let Insta_Url;
    export let LinkeIn_Url;
    export let Image;
</script>
<div class="card">
    <div class="front" style="background-image: url({Image});">
        <div class="container">
            <p class="name">{name}</p>
            <p class="job">{job}</p>    
        </div>
    </div>
    <div class="back">        
        <a href={GitHub_Url} target="_blank" class="links"> <img src="src\Assets\icons8-github-512.png" alt=""> {GitHub_User}</a>
        <a href={Insta_Url} target="_blank" class="links"> <img src="src\Assets\icons8-instagram-500.png" alt=""> {Insta_User}</a>
        <a href={LinkeIn_Url} target="_blank" class="links"> <img src="src\Assets\icons8-linkedin-500.png" alt=""> {LinkedIn_User}</a>
    </div>
</div>

<style>
.card{
    position: relative;
    margin-bottom: 5vw;
    transform-style: preserve-3d;
    transition: all 0.5s ease;
}

.card:hover{
    transform: rotateY(180deg);
}

.front{
    background-position:center;
    background-repeat: no-repeat;
    background-size: cover;
    position: absolute;
    border-radius: 1.8vw;
    width: 17vw;
    height: 30vw;
    display: flex;
    justify-content: center;
    align-items: end;
    backface-visibility: hidden;
    z-index: 1;
}

.container{
    border: 0.13vw solid rgb(169,121,50);
    border-radius: 0.5vw;
    width: 14.3vw;
    margin-bottom: 1.5vw;
    padding: 1.1vw 0vw 1vw 1.9vw;
    align-items: center;
    background-color: rgba(255,255,255,0.6);
    backdrop-filter: blur(0.3vw);
}

.container .name{
    font-family: "Nunito_Bold";
    font-size: 1.25vw;
    font-weight: 700;
    color: rgb(26,29,41);
}

.container .job{
    font-family: "Nunito_Bold";
    margin-top: 0.2vw;
    font-size: 1.15vw;
    color: rgb(177,120,37);
    font-weight: 600;
}

.back{
    background-image: url("D:/Apricity/src/Images/bg.png");
    border-radius: 1.8vw;
    width: 17vw;
    height: 30vw;
    display: flex;
    flex-direction: column;    
    align-items: center;
    justify-content: center;
    border: 0.2vw solid rgb(169,121,50);
    box-shadow: -0.15vw 0.25vw 0.4vw rgba(68, 68, 68, 0.3);
    transform: rotateY(180deg);
    backface-visibility: hidden;
}

.links{
    font-family: "Nunito_SemiBold";
    display: flex;
    align-items: center;
    border: 0.14vw solid rgb(169,121,50);
    border-radius: 0.7vw;
    margin: 0.5vw;
    padding-left: 0vw;
    width: 13.5vw;
    height: 2.7vw;
    color: rgb(169,121,50);
    text-decoration: none;
    font-weight:600;
    font-size: 1.2vw;
}
img{
  width: 3vw;
  padding: 0vw 0.6vw;
}

/* Tablet styles */
@media (max-width: 1024px) {
    .card{
        margin: 0 4vw 6vw 4vw;
    }

    .front, .back {
        width: 30vw;
        height: 50vw;
    }
    
    .container {
        width: 25vw;
        padding: 1.3vw 0 1.3vw 2vw;
    }
    
    .container .name {
        font-size: 2.5vw;
    }
    
    .container .job {
        font-size: 2.1vw;
    }
    
    .links {
        margin: 1vw;
        width: 26vw;
        height: 5vw;
        font-size: 2.3vw;
        padding: 3vw 0;
        border: 0.30vw solid rgb(169,121,50);
        border-radius: 1vw;
    }
    
    img {
        width: 6.3vw;
        padding: 0vw 1vw;
    }
}

/* Mobile styles */
@media (max-width: 480px) {
    .front, .back {
        width: 39vw;
        height: 70vw;
    }
    
    .container {
        width: 35vw;
        padding: 2vw 0vw 2vw 2vw;
        margin-bottom: 3vw;
        backdrop-filter: blur(1vw);
    }
    
    .container .name {
        font-size: 3.5vw;
    }
    
    .container .job {
        font-size: 3.1vw;
    }
    
    .links {
        width: 33vw;
        height: 8vw;
        font-size: 3vw;
        margin: 0.95vw;
        border-radius: 1.3vw;
    }
    
    img {
        width: 9.5vw;
        padding: 2vw 2vw;
    }
}
</style>