<script>
  import Form from "./Form.svelte";

  let showForm = false;
  function ClickHandeler(){
    showForm = !showForm;
    console.log("clicked")
  }
</script>

<Form {showForm} on:click={ClickHandeler}/>
<section>
    <section class="container">
        <div class="logo">APRICITY</div>
        <div class="caption">We're gonna build something <br> GREAT together !</div>
        <button on:click={ClickHandeler}>Become a client ?</button>
    </section>
    <section class="footer">
        <div>
            <div class="Title">Contact us</div><br>
            <div class="email">Email <br> apricityagency@gmail.com</div>
            <div class="phone">Phone Number <br> +963 454 242 153</div>
        </div> 
        <div>
            <div class="Title">Our socials</div>
            <div class="icons">
                <a href=""><img src="src\Assets\icons8-github-512.png" alt=""></a>
                <a href=""><img src="src\Assets\icons8-instagram-500.png" alt=""></a><br>
                <a href=""><img src="src\Assets\icons8-facebook-500.png" alt=""></a>
                <a href=""><img src="src\Assets\icons8-linkedin-500.png" alt=""></a><br>
                <a href=""><img src="src\Assets\icons8-telegram-app-512.png" alt=""></a>
                <a href=""><img src="src\Assets\icons8-whatsapp-512.png" alt=""></a>
            </div>
        </div>  
        <div>
            <div class="Title">Do you Have any problem ? <br> Let us know</div>
            <div class="input-group">
                <textarea placeholder="Type here"></textarea>
                <button><img src="src\Assets\icons8-send-96.png" alt="" class="send"></button>
            </div>
        </div>
    </section>
    
    <div class="coppyRights">©ApricityAgency2025.Allrights reserved</div>
</section>

<style>
section{
  background-color: rgb(6, 26, 50); 
  color: white;
  padding: 2vw 3vw 2vw 4vw;
  overflow: hidden;
}

.container{
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: white;
}

.footer{
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.logo{
  margin: 1vw;
  color: transparent;
  text-shadow: 0.15vw 0.17vw 0.8vw rgb(0, 0, 0, 0.8), 0 0 0 #E2A243;
  font-size: 2.1vw;
  font-weight: bold;
  font-family: "Title";
  letter-spacing: 0.05em;
}

.caption{
  margin: 3vw;
  text-align: center;
  color: white;
  font-size: 2.9vw;
  font-family: "Nunito_Bold";
}

.container button{
  font-family: "Nunito_SemiBold";
  cursor: pointer;
  font-size: 1.1vw;
  color:white;
  background: #c88d34;
  border: none;
  border-radius: 2vw;
  padding: 1.1vw 1.7vw;
}

.Title{
  font-family: "Nunito_Bold";
  color: #f6c274;
  font-size: 1.8vw;
}

.email{
  margin-bottom: 1.6vw;
}

.phone , .email{
  font-family: "Nunito_Regular";
  font-size: 1.9vw;
}

.icons img{
  width: 2.3vw;
  margin: 1.6vw 1vw 0vw 1vw;
}

.input-group {
  display: flex;
  justify-content: space-between;
  margin-top: 1vw;
  padding-bottom: 1vw;
  border-bottom: 0.1vw solid white;
}

.input-group textarea{
  height: auto;
  resize: none; 
  border: none;
  background-color:rgb(6, 26, 50);
  color: white;
  font-size: 1vw;
  outline: none;
  field-sizing: content;
  padding: 0;
  width: 20vw;
  max-height: 8vw;
}

.input-group textarea::-webkit-scrollbar{
  width: 0;
}

.input-group button {
  background: rgb(6, 26, 50);
  border: none;
  cursor: pointer;
  padding: 0;
  align-items: flex-end;
  justify-content: flex-end;
}

.send{
  width: 1.5vw;
}

.coppyRights{
  margin: 0rem 2.1vw;
  border-top: 0.1vw solid white;
  display: flex;
  justify-content: center;
  font-size: 1.1vw;
  padding-top: 1.1vw;
  letter-spacing: 1px;
  color: white;
}

/* Tablet styles */
@media (max-width: 1024px) {
  section {
    padding: 3vw 2.5vw;
  }

  .logo{
    margin: 0;
    font-size: 5vw;
  }
  
  .caption {
    font-size: 3vw;
    margin: 4vw 0;
  }

  .container button{
    font-size: 1.8vw;
    border-radius: 2.5vw;
    padding: 1.3vw 1.4vw;
  }

  .email , .phone{
    font-size: 2.6vw;
  }
  
  .Title {
    font-size: 2.5vw;
  }

  .icons img{
    width: 3.8vw;
    margin: 2vw 1.2vw 0 1.2vw;
  }

  .input-group{
    margin-top: 2.4vw;
    padding-bottom: 1.2vw;
  }
  
  .input-group textarea {
    width: 27vw;
    font-size: 2vw;
    max-height: 11vw;
  }

  .send{
    width: 2.3vw;
  }

  .coppyRights{
    font-size: 1.8vw;
    padding-top: 1.5vw;
  }
}

/* Mobile styles */
@media (max-width: 480px) {
  section {
    padding: 4vw 4vw 2vw 3vw;
  }

  .logo {
    text-shadow: 0.6vw 0.3vw 1.7vw rgb(0, 0, 0, 0.8), 0 0 0 #E2A243;
    font-size: 9vw;
  }
  
  .caption {
    font-size: 5vw;
    margin: 8vw;
  }
  .container button{
    border-radius: 6vw;
    padding: 2vw 3vw;
    font-size: 3.5vw;
    margin-bottom: 6vw;
  }
  
  .phone , .email{
    font-size: 4vw;
  }
  .email{
    margin-bottom: 4vw;
  }
  
  .Title {
    font-size: 4.4vw;
    margin: 0;
  }

  div{
    margin-bottom: 4vw;
  }

  .icons img {
    width: 6.3vw;
    margin: 3vw 3vw 0 2vw;
  }

  .input-group{
    margin-top: 4vw;
  }
  
  .input-group textarea {
    font-size: 3.2vw;
    width: 70vw;
    max-height: 15vw;
    margin-right: 2vw;
  }
  .send{
    width: 4vw;
  }
  
  .coppyRights {
    margin: 0 3vw 2vw 3vw;
    font-size: 3vw;
    padding-top: 2vw;
  }
}
</style>