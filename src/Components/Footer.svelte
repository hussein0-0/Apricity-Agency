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
            <div>Phone Number <br> +963 454 242 153</div>
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
  padding: 2rem 3rem 2rem 4rem;
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
}

.logo{
  margin: 1rem;
  color: transparent;
  text-shadow: 10px -4px 15px rgb(0, 0, 0, 0.8), 0 0 0 #E2A243;
  font-size: 2rem;
  font-weight: bold;
  font-family: "Title";
  letter-spacing: 0.05em;
}

.caption{
  margin: 3rem;
  text-align: center;
  color: white;
  font-size: 2.8rem;
  font-family: "Nunito_Bold";
}

.container button{
  font-family: "Nunito_SemiBold";
  cursor: pointer;
  font-size: 1rem;
  color:white;
  background: #c88d34;
  border: none;
  border-radius: 2rem;
  padding: 1em 1.6em;
}

.Title{
  font-family: "Nunito_Bold";
  color: #f6c274;
  font-size: 1.7rem;
}

.email{
  margin-bottom: 18px;
}

div{
  font-family: "Nunito_Regular";
  font-size: 1.8rem;
}

.icons img{
  width: 2.2rem;
  margin: 1.5rem 15px 0 15px;
}

.input-group {
  display: flex;
  justify-content: space-between;
  margin-top: 1.5rem;
  border-bottom: 3px solid white;
}

.input-group textarea{
  height: auto;
  resize: none; 
  border: none;
  background-color:rgb(6, 26, 50);
  color: white;
  font-size: 1rem;
  outline: none;
  field-sizing: content;
  padding: 0;
  width: 19.6rem;
  max-height: 9.4rem;
}

.input-group textarea::-webkit-scrollbar{
  width: 0;
}

.input-group button {
  background: rgb(6, 26, 50);
  border: none;
  cursor: pointer;
  padding: 0;
}

.send{
  width: 1.4rem;
}

.coppyRights{
  margin: 0rem 2rem;
  border-top: 1px solid white;
  display: flex;
  justify-content: center;
  font-size: 1rem;
  padding-top: 1rem;
  letter-spacing: 1px;
  color: white;
}

</style>