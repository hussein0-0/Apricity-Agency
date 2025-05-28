<section>
    <div class="wave-container">
        <svg class="top"  viewBox="0 0 1440 320">
            <path fill="rgb(206, 150, 6)"  fill-opacity="1" 
                d="M0,160L60,133.3C120,107,240,53,360,42.7C480,32,600,64,720,101.3C840,139,960,181,1080,192C1200,203,1320,181,1380,170.7L1440,160L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z">
            </path>
        </svg>
        <svg class="second" viewBox="0 0 1440 320">
            <path fill="rgb(206, 150, 6)" fill-opacity="0.5" 
                d="M0,160L48,149.3C96,139,192,117,288,133.3C384,149,480,203,576,240C672,277,768,299,864,277.3C960,256,1056,192,1152,181.3C480,0,384,0,288,0">
            </path>
        </svg>
        <svg class="third" viewBox="0 0 1440 320">
            <path fill="rgb(206, 150, 6)" fill-opacity="0.4" 
                d="M0,160L60,181.3C120,203,240,245,360,240C480,235,600,181,720,144C840,107,960,85,1080,64C1200,43,1320,21,1380,10.7L1440,0L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z">
            </path>
        </svg>
    </div>
    <div class="title">Our Team</div>
</section>

<style>
section{
    position: relative;
    background-color: rgb(6, 26, 50);
}

.wave-container{
    overflow: hidden;
}

.top{
    position: absolute;
    z-index: 1;
}

.second{
    position: absolute;
    z-index: 2;
}
.title{
    color:rgb(206, 150, 6);
    font-size: 7rem;
    font-weight: 900;
    display: flex;
    justify-content: center;
}
</style>