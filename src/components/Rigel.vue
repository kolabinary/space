<template>
  <div class="rigel-container">
    <nav class="header">
      <router-link to="/"><img src="../assets/img/back.svg" class="back" alt="back to home"></router-link>
    </nav>
    <div class="hero">
      <h1>rigel<span style="color: #0034B9">.</span> </h1>
      <p>Four habitable planets detected</p>
      <section class="halo">
        <a class="hvr-sweep-to-left" href="#">Enter Orbit</a>
      </section>

    </div>
  </div>
</template>

<script>
export default {
  name: 'rigel',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >


  .rigel-container {
    color: #fff;
    background-color: #000;
    height: calc(100vh);
    padding: 0 8%;
    background-image: url('../assets/img/rigel.png'), url('../assets/img/back-drop.svg');
    background-position: 150% 50%;
    background-repeat: no-repeat;
    background-size: 900px, cover;
  }

    .header {
      padding: 3% 0;

    }

    .header img {
      width: 4%;
    }

    .hero  p {
      margin: 0;
      font-size: 1.2rem;
      letter-spacing: 1px;
    }

    .hero h1 {
      font-size: 150px;
      font-weight: 500;
      margin: 0;
    }

    .halo  a {
      color: #325EE0;
      letter-spacing: 2px;
      text-decoration: none;
      border: 2px solid #325EE0;
      border-radius: 35px;
      padding: 1.5rem 4rem;
      font-weight: 700;

    }

    .halo  a:hover {
      /*background-color: #7842F0;*/
      color: #fff;
    }

    .halo {
      padding: 2% 0 0 0;
      margin-top: 50px;
    }


  .hvr-sweep-to-left {
    display: inline-block;
    vertical-align: middle;
    -webkit-transform: perspective(1px) translateZ(0);
    transform: perspective(1px) translateZ(0);
    box-shadow: 0 0 1px rgba(0, 0, 0, 0);
    position: relative;
    -webkit-transition-property: color;
    transition-property: color;
    -webkit-transition-duration: 0.3s;
    transition-duration: 0.3s;
    border-radius: 35px;
    color: #000;
  }

  .hvr-sweep-to-left:before {
    content: "";
    position: absolute;
    z-index: -1;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background:#325EE0;
    -webkit-transform: scaleX(0);
    transform: scaleX(0);
    -webkit-transform-origin: 100% 50%;
    transform-origin: 50% 50%;
    -webkit-transition-property: transform;
    transition-property: transform;
    -webkit-transition-duration: 0.3s;
    transition-duration: 0.3s;
    -webkit-transition-timing-function: ease-out;
    transition-timing-function: ease-out;
    border-radius: 35px;
  }
  .hvr-sweep-to-left:hover, .hvr-sweep-to-left:focus, .hvr-sweep-to-left:active {
    color: #fff;
    border-radius: 35px;
  }
  .hvr-sweep-to-left:hover:before, .hvr-sweep-to-left:focus:before, .hvr-sweep-to-left:active:before {
    -webkit-transform: scaleX(1);
    transform: scaleX(1);
    border-radius: 35px;
  }


  @media only screen and (max-width: 500px){
    .hero h1 {
      font-size: 90px;
      line-height: 0.8;
    }

    .header img {
      width: 15%;
    }

    .hero  p {
      margin-top: 2rem;
    }

    .rigel-container {
      padding-top:35px;
      background-position: 85% 211%;
      background-size: 750px, cover;
    }

    .hero {
      margin-top: 3rem;
    }

    .halo a {
      display: block;
      text-align: center;
    }
  }



</style>
