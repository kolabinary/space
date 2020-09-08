 <template>
  <div class="container">

    <div :class="{'toggle-bar2' : visible, 'toggle-bar' : !visible}" v-on:click="seen = !seen, visible = !visible"></div>
    <div class="menu" v-if="seen">
      <div class="astro" style="text-align: center; margin-right:15px; width: 30%;">
        <img src="../assets/img/astro.svg" alt="">
        <p style="font-size: 25px; color: #000; font-weight: 600; margin: 0; letter-spacing: 2px">The Launch Pad</p>
      </div>
     <ul>
       <li class="system">STAR SYSTEM</li>
       <li><router-link to="/rigel">Rigel</router-link></li>
       <li><a href="">GAMMA ANDROMEDAE</a></li>
       <li><a href="">Canis Majoris</a></li>
       <li><a href="">Alpha Centuari</a></li>
     </ul>
    </div>

    <nav class="header">
      <div><img src="../assets/img/orion-logo.svg" alt=""></div>
      <!--<div><img src="../assets/img/menu.svg" alt=""></div>-->
    </nav>

    <section class="hero">
      <div><h6 style="color: #fff;">Welcome to Orion 5</h6></div>
      <div><h1><span style="color: #7842F0;">No</span> gravity</h1></div>
    </section>

    <section class="halo">
    <router-link class="hvr-sweep-to-left" to="/join" >WARP DRIVE </router-link>
    </section>
    
    <footer class="foot">

      <div class="planet">

        <div></div>
        <img class="beam" src="../assets/img/moon.svg" alt="">

      </div>

    </footer>




  </div>
</template>

<script>



export default {
  name: 'home',

    data: function () {
        return {
            seen:false,
            visible:true
        }
    }
      
    }


</script>



<style scoped>

  @import '../../public/style.css';

  * {
    font-family: 'TT Norms Pro', 'sans-serif';
  }

  .container {
    background-image: url('../assets/img/back-drop.svg');
    background-size: cover;
    color: #fff;
    background-color: #000;
    height: calc(100vh);
    padding: 0 8%;

  }
    .header {
      padding: 3% 0;
      display: flex;
      justify-content: space-between;
    }

    .header  img {
      width: 80%;
    }

    .hero h6 {
      font-size: 25px;
      font-weight: 200;
      margin-top: 0;
      letter-spacing: 2px;
    }
    .hero h1 {
      font-size: 150px;
      margin: 0;
      margin-top: -50px;
      font-weight: 400;
    }
    .hero {
      padding-top: 8%;
    }

    .halo  a {
      color: #7842F0;
      letter-spacing: 2px;
      text-decoration: none;
      border: 2px solid #7842F0;
      border-radius: 35px;
      padding: 1.5rem 4rem;
      font-weight: 500;
    }

    .halo a:hover {
      /*background-color: #7842F0;*/
      color: #fff;
    }

    .halo {
      padding: 2% 0 0 0;

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
    background: #7842F0;
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

  footer {
    position: fixed;
    bottom: 0;
    width: 100%;
  }

  .beam {
    /*box-shadow: 5px 10px 10px rgba(237, 176, 12, 0.4);*/
    opacity: 1;
    animation: beam 1s infinite;
    animation-timing-function: ease-in-out;
  }



  .planet {
      background: url('../assets/img/planet.svg');
      /*width: 100%;*/
      background-repeat: no-repeat;
      background-size:67%;
      /*padding: 10% 0;*/
      background-position: 30% 20%;
      height: 150px;
      animation: bounce 3s infinite;
      animation-timing-function: ease-in-out;
      display:flex;
      justify-content: space-between;
      padding: 0 10%;
  }

  @keyframes bounce {
    0% {background-position: 30% 20%;}
    50% {background-position: 30% 25%;}
    100% {background-position: 30% 20%;}
  }
  @keyframes beam {
    0% {opacity: 1;}
    50% {opacity: 0.7;}
    100% {opacity: 1;}
  }

  .menu {
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    background: #7842F0;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    z-index: 1000;
    overflow-y: auto;
    transition: 0.5s ;
    animation: menu 1s ;
    transform:scale(1, 1);
    animation-timing-function: ease-in-out;
    padding: 0 5%;
  }

  @keyframes menu {
    0% {transform:scale(0,0);}
    25% {transform:scale(0.7,0.7);}
    50% {transform:scale(0.9,0.9);}
    100% {transform:scale(1,1);}
  }

  .menu ul {
    position: relative;
    margin-left: 100px;
  }

  .menu li {
    position: relative;
    list-style: none ;
    display: block;
    padding: 2% 0;

  }

  .menu ul li a {
    color: #fff;
    text-decoration: none;
    text-transform: uppercase;
    display: inline-block;
    font-size: 30px;
    font-weight: 400;
    letter-spacing: 1px;

  }

  .menu ul li a::before {
    position: absolute;
    content: '';
    top: 50%;
    left: 0;
    width: 100%;
    background: #EDB00C;
    height: 8px;
    transform: translateY(-50%) scaleX(0);
    transform-origin: right;
    transition: 0.5s transform;
  }

  .menu ul li a:hover::before{
    transform: translateY(-50%) scaleX(1);
    transform-origin: left;
    transition: 0.5s transform;

  }
  .toggle-bar {
    background: url('../assets/img/close.svg');
    background-repeat: no-repeat;
    background-position: center;
    color: white;
    position: fixed;
     top: 20px;
    right: 20px;
    width: 50px;
    height: 50px;
    background-color: #000;
    z-index: 1001;
    border-radius: 50px;
    cursor: pointer;
    margin-right: 5%;
  }

  .toggle-bar2 {
    background: url('../assets/img/menu.svg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: 80%;
    /*color: white;*/
    position: fixed;
    top: 20px;
    right: 20px;
    width: 50px;
    height: 50px;
    background-color: #000;
    z-index: 1001;
    border-radius: 50px;
    cursor: pointer;
    margin-right: 5%;
  }
  .system {
    color: #000;
    font-size: 30px;
    border-bottom: 1px solid black;
    max-width: 12ch;
    font-weight: 600;
    margin-bottom: 20px;
  }




@media only screen and (max-width: 500px) {
  .container {
    height: 100vh;
  }

  .header {
    padding-top: 2rem;
  }

  .hero {
    margin-top: 5rem;
  }

  .hero h1 {
    font-size: 90px;
    line-height: 0.8;
  }

  .hero h1 > span {
    display: block;
  }

  .hero > div {
    margin-bottom: 5rem;
  }

  .toggle-bar2 {
    right: 0;
  }

  .astro {
    text-align: center;
    /* margin-right: 15px; */
    width: 50% !important;
    /* display: none; */
    position: absolute;
    top: 90px;
    right: 100px;
  }

  .astro img {
    height: 70px;
  }

  .astro p {
    font-size: 18px !important;
  }

  .menu ul {
    margin-left: 0;
  }

  .menu ul li a {

    font-size: 25px;
    font-weight: 400;
    letter-spacing: 1px;

  }

  .halo a {
    display: block;
    text-align: center;
  }

  .beam {
    height: 36px;
  }

}





</style>
