<script>
    export let showForm;
</script>

{#if showForm}
<div class="background">
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
    backdrop-filter: blur(8px);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10;
    top: 0;
    left: 0;
}
.Form{
    position: relative;
    border-radius: 10px;
    width: 40rem;
    background-color: white;
    padding: 1rem 3rem 0rem 3rem;
    height: 90vh;
    overflow: auto;
    z-index: 11;
}
.header{
    text-align: center;
    margin: 0;
    font-size: 2rem;
    color: goldenrod;
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
    color: goldenrod;
    border: none;
    font-size: 1.5rem;
    cursor: pointer;
    margin: 1rem 2rem 0rem 0rem;
}
.header .title{
    font-weight: bold;
}
input , select{
    background-color: rgb(226, 226, 226);
    border: none;
    border-radius: 0.6rem;
    width: 100%;
    height: 2rem;
    margin: 0.4rem 0rem;
    padding-left: 0.5rem;
}
div{
    margin: 1rem 0rem;
}
label{
    font-size: 1.2rem;
}
textarea{
    min-height: 2rem;
    height: auto;
    resize: none; 
    border: none;
    background-color: rgb(226, 226, 226);
    border: none;
    border-radius: 0.6rem;
    width: 100%;
    margin: 0.4rem 0rem;
    padding: 0.5rem;
    font-size: 1rem;
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
    margin:0.5rem 0.4rem 0rem 0.4rem;
    width: 7rem;
    height: 3rem;
    border-radius: 2rem;
    cursor: pointer;
}
.buttons .send{
    font-size: 1rem;
    color: white;
    background-color: goldenrod;
    border: none;
}
.buttons .cencel{
    color: goldenrod;
    background-color: white;
    border: 2px solid goldenrod;
}
</style>