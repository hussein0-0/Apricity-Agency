<section id="WhyUs">
<svg class="curve-divider" viewBox="0 0 100 1000" preserveAspectRatio="none">
  <defs>
    <linearGradient id="fadeFill" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="rgb(122, 57, 4)" stop-opacity="1" />
      <stop offset="100%" stop-color="rgb(122, 57, 4)" stop-opacity="0" />
    </linearGradient>
  </defs>

  <path
    d="M25 0
       C75 150, 15 300, 25 500
       C25 650, 70 850, 30 1000
       L40 1000
       C85 850, 35 650, 40 500
       C40 300, 85 150, 35 0
       Z"
    fill="url(#fadeFill)"
  />
</svg>


  <div class="row">
    <div class="cell left"></div>
    <div class="cell right"></div>
    <!-- empty right cell -->
  </div>

  <div class="row">
    <div class="cell left">
      <h3>
        We're not just a digital agency — we're a <span>team</span> that <br />
        believed in an idea and turned it into a project built on <br />
        passion, dedication, and genuine <span>love for what we do</span>.
      </h3>
    </div>
    <div class="cell right"></div>
    <!-- empty right cell -->
  </div>

  <div class="row">
    <div class="cell left"></div>
    <!-- empty left cell -->
    <div class="cell right">
      <h3>
        That's why our services are always: <br />
        1. <span>Fast and organized</span> — because we value your time <br />
        2. <span>Smooth and professional</span> — because you deserve a <br />
        seamless collaboration
      </h3>
    </div>
  </div>

  <div class="row">
    <div class="cell left">
      <h3>
        <span>Creative and thoughtful</span> — because details make all <br />
        the difference <br />
        <span>Responsible and committed</span> — because we never <br />
        compromise on quality
      </h3>
    </div>
    <div class="cell right"></div>
  </div>

  <div class="row">
    <div class="cell left"></div>
    <div class="cell right">
      <h3>
        Our goal is to craft unique digital solutions that <br />
        reflect <span>your vision</span>, support <span>your goals</span>, and
        leave a <br />
        <span>lasting impression</span>.
      </h3>
    </div>
  </div>
</section>

<style>
  #WhyUs {
    position: relative; /* so curve positions relative to section */
    display: grid;
    gap: 2vw;
    background-color: rgb(230, 161, 58);
    padding: 2vw;
    color: #fff;
  }

  .curve-divider {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 50%; /* center between columns */
    width: 14vw; /* thickness of divider */
    height: 100%; /* full height of section */
    transform: translateX(-50%);
    z-index: 0; /* behind the text */
  }

  section {
    display: grid;
    gap: 2vw;
    background-color: rgb(230, 161, 58);
    padding: 2vw;
    color: #fff;
  }

  .row {
    display: grid;
    grid-template-columns: 1fr 1fr; /* always 2 columns */
    gap: 4vw;
    margin-bottom: 4vw;
  }
  .row:last-child {
    margin-bottom: 0;
  }

  .cell h3 {
    font-family: "Nunito_Regular";
    font-size: 1.8vw;
    color: rgb(122, 57, 4);
  }

  .cell span {
    font-family: "Nunito_Regular";
    padding: 1vw 0;
    font-size: 1.8vw;
    color: rgb(17, 12, 5);
    font-weight: 700;
  }

  /* Responsive */
  @media (max-width: 1024px) {
    .row {
      grid-template-columns: 1fr; /* stack columns on tablet */
    }
    .cell h3,
    .cell span {
      font-size: 2.7vw;
    }
  }

  @media (max-width: 480px) {
    .cell h3,
    .cell span {
      font-size: 3.6vw;
    }
  }
</style>
