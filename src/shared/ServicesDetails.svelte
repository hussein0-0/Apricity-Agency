<script>
    export let Title;
    export let Disc;
</script>

<div class="container">
    <div class="title"><p> <img src="src\Assets\icons8-bulb-384.png" alt=""> {Title}</p></div>
    <div class="disc"><p>{Disc}</p></div>
</div>


<style>
.container{
  position: relative;
  padding: 7.4vw 0vw;
  margin: 0vw 3.2vw ;
}

.title{
  position:absolute;
  color: #ffffff;
  border: 0.3vw solid rgb(11, 27, 49);
  border-radius: 5.2vw;
  background-color: rgb(11, 27, 49);
  z-index: 0;
  width: 51vw;
  height: 12.55vw;
  display: flex;
  align-items: center;
  z-index: 1;
}

.disc{
  position:absolute;
  right: 0;
  color: rgb(11,27,49);
  border: 0.3vw solid rgb(11, 27, 49);
  border-radius: 5.2vw;
  background-color: rgb(11,27,49,0.1);
  width: 51vw;
  height: 12.55vw;
  display: flex;
  align-items: center;
  text-align: start;
}

.title p{
  font-family: "Nunito_Bold";
  text-align: left;
  font-size: 2.3vw;
  font-weight: bold;
  padding-left: 2.1vw;
}

.disc p{
  font-family: "Poppins_Regular";
  font-size: 1.7vw;
  font-weight: 500;
  padding: 0vw 3vw 0vw 11.2vw;

}
img{
  width: 2.3vw;
  margin: 0vw 1vw;
}

/* Tablet styles */
@media (max-width: 1024px) {
  .container{
    padding: 8.4vw 0vw;
    margin: 2vw 2vw;
  }
  .title , .disc{
    width: 52.5vw;
    height: 15vw;
  }
  .title p{
    font-size: 2.4vw;
    padding-left: 1.3vw;
  }
  .disc p{
    font-size: 1.85vw;
    padding: 0vw 3vw 0vw 13vw;
  }
  img{
    width: 2.5vw;
    margin: 0vw 0.8vw;
  }
}

/* Mobile styles */
@media (max-width: 480px) {
  .container{
    margin-top: 7vw;
    padding: 0;
  }
  .title{
    position: relative;
    width: 100%;
    margin-bottom: -9vw;
    height: 22vw;
    border-radius: 4vw;
  }
  .disc{
    position: relative;
    width: 100%;
    height: 22vw;
    border-radius: 4vw;
  }
  .title p{
    font-size: 4.5vw;
  }
  .disc p{
    padding: 8vw 2vw 0vw 3vw;
    font-size: 3vw;
  }
  img{
    width: 4.3vw;
    margin: 0vw 1.2vw;
  }
}

</style>