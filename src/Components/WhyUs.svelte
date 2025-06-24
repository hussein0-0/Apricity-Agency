<section id="WhyUs">
  <h2>WHY US</h2>
  <div class="left">
    <div class="container">
      <h3>We're not just a digital agency — we're a <span>team</span> that <br> 
          believed in an idea and turned it into a project built on <br>
          passion, dedication, and genuine <span>love for what we do</span>.
      </h3>
    </div>
  </div>

  <div class="right">
    <div class="container">
      <h3>That's why our services are always: <br>
          1. <span>Fast and organized</span> — because we value your time <br> 
          2. <span>Smooth and professional</span> — because you deserve a <br>
          seamless collaboration
        </h3>
    </div>
  </div>

  <div class="left">
    <div class="container">
      <h3>3. <span>Creative and thoughtful</span> — because details make all <br>
          the difference <br>
          4. <span>Responsible and committed</span> — because we never <br>
          compromise on quality
      </h3>
    </div>
  </div>

  <div class="right">
    <div class="container">
      <h3>Our goal is to craft unique digital solutions that <br>
          reflec <span>your vision</span>, support <span>your goals</span>, and leave a <br>
          <span>lasting impression</span>.
      </h3>
    </div>
  </div>
</section>

<style>
section {
  position: relative;
  background-color: rgb(230, 161, 58);
  color: #fff;
  margin: -0.2vw 0;
  padding: 2vw 2vw;
  z-index: 1;
}
h2{
  font-size: 4vw;
}

.container{
  text-align: left;
}
.left {
  display: flex;
  padding: 4.2vw 2.2vw;
  left: 0;
}

.right {
  right: 0;
  display: flex;
  justify-content: flex-end;
}

.container h3{
  font-family: "Nunito_Regular";
  font-size: 2.1vw;
  color: white;
}

.container span{
  font-family: "Nunito_Regular";
  padding: 1vw 0vw;
  font-size: 2.1vw;
  color: rgb(67,47,16);
  font-weight: 700;
}

/* Tablet styles */
@media (max-width: 1024px) {
  .left , .right{
    padding: 4vw 2.2vw;
  }
  .container h3{
    font-size: 2.7vw;
  }
  .container span{
    font-size: 2.7vw;
  }
}

/* Mobile styles */
@media (max-width: 480px) {
  .left , .right{
    justify-content: left;
  }
  .container h3{
    font-size: 3.6vw;
  } 
  .container span{
    font-size: 3.6vw;
  }
}
</style>