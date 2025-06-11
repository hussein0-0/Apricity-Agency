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
  padding: 7.2rem 0rem;
  margin: 0rem 3rem ;
}

.title{
  position:absolute;
  color: #ffffff;
  border: 4px solid rgb(11, 27, 49);
  border-radius: 5rem;
  background-color: rgb(11, 27, 49);
  z-index: 0;
  width: 49rem;
  height: 12.05rem;
  display: flex;
  align-items: center;
  z-index: 1;
}

.disc{
  position:absolute;
  right: 0;
  color: rgb(11,27,49);
  border: 4px solid rgb(11, 27, 49);
  border-radius: 5rem;
  background-color: rgb(11,27,49,0.1);
  width: 49rem;
  height: 12.05rem;
  display: flex;
  align-items: center;
  text-align: start;
}

.title p{
  font-family: "Nunito_Bold";
  text-align: left;
  font-size: 2.2rem;
  font-weight: bold;
  padding-left: 2rem;
}

.disc p{
  font-family: "Poppins_Regular";
  font-size: 1.6rem;
  font-weight: 500;
  padding: 0 3rem 0 11rem;

}
img{
  width: 2.1rem;
  margin: 0rem 1rem;
}
</style>