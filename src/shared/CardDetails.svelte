<script>
    export let name;
    export let job;
    export let Insta_User;
    export let GitHub_User;
    export let LinkedIn_User;
    export let GitHub_Url;
    export let Insta_Url;
    export let LinkeIn_Url;
</script>
<div class="card">
    <div class="front">
        <div class="container">
            <p class="name">{name}</p>
            <p class="job">{job}</p>    
        </div>
    </div>
    <div class="back">        
        <a href={GitHub_Url} target="_blank" class="links"> <i class="fa-brands fa-github " style="color: rgb(6, 26, 50);"></i> {GitHub_User}</a>
        <a href={Insta_Url} target="_blank" class="links"> <i class="fa-brands fa-instagram " style="color: rgb(6, 26, 50);"></i> {Insta_User}</a>
        <a href={LinkeIn_Url} target="_blank" class="links"> <i class="fa-brands fa-linkedin " style="color: rgb(6, 26, 50);"></i> {LinkedIn_User}</a>
    </div>
</div>

<style>
.card{
    position: relative;
    margin-bottom: 5rem;
    transform-style: preserve-3d;
    transition: all 0.5s ease;
}

.card:hover{
    transform: rotateY(180deg);
}

.front{
    position: absolute;
    background-color: rgb(231, 231, 231);
    border-radius: 1.7rem;
    width: 15.5rem;
    height: 28.4rem;
    display: flex;
    justify-content: center;
    align-items: end;
    backface-visibility: hidden;
    z-index: 1;
}

.container{
    border: 1.6px solid rgb(169,121,50);
    border-radius: 0.4rem;
    width: 13.8rem;
    margin-bottom: 1.4rem;
    padding: 1rem 0rem 1rem 1.8rem;
    align-items: center;
    background-color:rgb(231, 231, 231) ;
}

.container .name{
    font-family: "Nunito_Bold";
    font-size: 1.2rem;
    font-weight: 700;
    color: rgb(26,29,41);
}

.container .job{
    font-family: "Nunito_Bold";
    margin-top: 3px;
    font-size: 1.1rem;
    color: rgb(177,120,37);
    font-weight: 600;
}

.back{
    background-color: rgb(255, 255, 255);
    border-radius: 1.7rem;
    width: 15.5rem;
    height: 28rem;
    display: flex;
    flex-direction: column;    
    align-items: center;
    justify-content: center;
    border: 3px solid rgb(169,121,50);
    box-shadow: -4px 4px 5px rgba(68, 68, 68, 0.3);
    transform: rotateY(180deg);
    backface-visibility: hidden;
}

.links{
    font-family: "Nunito_SemiBold";
    display: flex;
    align-items: center;
    border: 2px solid rgb(169,121,50);
    border-radius: 0.6rem;
    margin: 8px;
    padding-left: 1rem;
    width: 13rem;
    height: 2.4rem;
    color: rgb(169,121,50);
    text-decoration: none;
    font-weight:600;
}

.links i{
    font-size: 1.3rem;
    margin-right: 20px;
}
</style>