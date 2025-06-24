<script>
    export let showForm;
</script>

{#if showForm}
<div class="background" on:click|self>
    <div class="Form">
        <form action="">
            <div class="header">
                <p class="title">Hey my friend,</p>
                <p> Let us know how we can help you!</p>
                <button class="close" on:click>X</button>
            </div>
            <div>
                <label for="Name">Name</label> <br>
                <input type="text" placeholder="Your Name" required>
            </div>    
            <div>
                <label for="Contact-Number">Contact Number</label> <br>
                <input type="tel" placeholder="+000 000 000 000" required>
            </div>    
            <div>
                <label for="Email">Email Address</label> <br>
                <input type="email" placeholder="email@gmail.com" required>
            </div>   
            <div>
                <label for="Service">What service are you interested in?</label> <br>
                <select name="Service" id="Service" required>
                    <option value="" disabled selected>Select service</option>
                    <option value="Web-App">Web App</option>
                    <option value="Application">Application</option>
                </select>
            </div> 
            <div>
                <label for="Brand-Name">Brand Name</label> <br>
                <input type="text" placeholder="Apricity" required>
            </div>    
            <div>
                <label for="Details">Tell us more about your request</label> <br>
                <textarea placeholder="Enter text..." required></textarea>
            </div>
            <div class="buttons">
                <input type="button" class="cencel" value="Cencel" on:click>
                <input type="submit" class="send" value="Send">
            </div>
        </form>
    </div>
</div>
{/if}

<style>
.background{
    margin: 0;
    width: 100%;
    height: 100vh;
    position: fixed;
    background-color: rgb(0, 0, 0, 0.25);
    backdrop-filter: blur(0.5rem);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10;
    top: 0;
    left: 0;
}
.Form{
    position: relative;
    border-radius: 1vw;
    width: 42rem;
    background-color: white;
    padding: 1vw 3vw 0vw 3vw;
    height: min(91vh , 47rem);
    overflow: auto;
    z-index: 11;
}
.header{
    text-align: center;
    margin: 0;
    font-size: 2rem;
    color: rgb(230, 161, 58);
    display: flex;
    flex-direction: column;
    align-items: center;
    line-height: 3rem;
}
.header .close{
    position: absolute;
    top: 0;
    right: 0;
    background-color: transparent;
    color: rgb(230, 161, 58);
    border: none;
    font-size: 1.6rem;
    cursor: pointer;
    margin: 1rem 2rem 0 0;
}
.header .title{
    font-weight: bold;
}
input , select{
    font-size: 1rem;
    background-color: rgb(226, 226, 226);
    border: none;
    border-radius: 0.6rem;
    width: 100%;
    height: 2.3rem;
    margin: 0.3rem 0;
    padding-left: 0.6rem;
}
div{
    margin: 1rem 0;
}
label{
    font-size: 1.2rem;
}
textarea{
    min-height: 2.3rem;
    height: auto;
    resize: none; 
    border: none;
    background-color: rgb(226, 226, 226);
    border: none;
    border-radius: 0.6rem;
    width: 100%;
    margin: 0.3rem 0;
    padding: 0.55rem;
    font-size: 0.9rem;
    field-sizing: content;
}
textarea::-webkit-scrollbar{
  width: 0;
}
.buttons{
    display: flex;
    justify-content: end;
}
.buttons input{
    padding: 0;
    margin:0.5rem 0.4rem 0 0.4rem;
    width: 7.2rem;
    height: 3.3rem;
    border-radius: 2rem;
    cursor: pointer;
}
.buttons .send{
    font-size: 1.1rem;
    color: white;
    background-color: rgb(230, 161, 58);
    border: none;
}
.buttons .cencel{
    font-size: 1.1rem;
    color: rgb(230, 161, 58);
    background-color: white;
    border: 0.1rem solid rgb(230, 161, 58);
}

/* Tablet styles */
@media (max-width: 1024px) {
    .Form {
        border-radius: 2rem;
        width: 40rem;
        padding: 1rem 2rem 0 2rem;
    }
    
    .header {
        font-size: 1.8rem;
        line-height: 2.4rem;
    }
    
    .header .close {
        font-size: 1.5rem;
        margin: 0.8rem 1.4rem 0 0;
    }
    
    input, select {
        margin: 0.3rem 0;
        padding-left: 1vw;
        border-radius: 2vw;
        height: 2.4rem;
        font-size: 0.9rem;
    }
    
    textarea {
        padding-left: 1vw;
        border-radius: 2vw;
        align-content: center;
        min-height: 2.4rem;
        font-size: 0.8rem;
    }
    
    label {
        padding-left: 0.3rem;
        font-size: 1.3rem;
    }

    div{
        margin: 1rem 0;
    }

    .buttons input{
        padding: 0;
        margin:0.3rem 0.4rem 0 0.4rem;
        width: 6.3rem;
        height: 3rem;
        border-radius: 2rem;
    }
    .buttons .send{
        font-size: 1rem;
    }
    .buttons .cencel{
        font-size: 1rem;
    }
}

/* Mobile styles */
@media (max-width: 480px) {
    .Form {
        border-radius: 6vw;
        width: 90%;
        padding: 3vw 3.5vw 0 3.5vw;
        height: 78.2vh;
    }
    
    .header {
        font-size: 5.9vw;
        line-height: 9vw;
    }
    
    .header .close {
        font-size: 6vw;
        margin: 2.5vw 4.5vw 0 0;
    }

    div{
        margin: 5vw 0;
    }
    
    input, select {
        margin: 0.9vw 0;
        height: 8vw;
        font-size: 4vw;
        border-radius: 2vw;
        padding-left: 1.2vw;
        width: 84vw;
    }
    option{
        display: flex;
    }
    textarea {
        padding-left: 1.2vw;
        border-radius: 2vw;
        font-size: 4vw;
        min-height: 8vw;
        align-content: center;
    }
    
    label {
        font-size: 5vw;
    }
    .buttons input {
        width: 20vw;
        height: 9vw;
        font-size: 5vw;
        margin: 2vw 2vw 0.9vw 2vw;
    }
    .buttons .send{
        font-size: 4vw;
    }
    .buttons .cencel{
        font-size: 4vw;
    }
}
</style>