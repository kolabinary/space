<template>
  <div class="container">
    
    <div class="card">
      
      <div class="pilot">
        <!--<img src="../assets/img/astro-white.svg" alt="" height="50">-->
      </div>

      <form action="">

        <div class="form-field">
          <label for="const">Constellation</label>
          <input id="const" type="text" placeholder="Constellation" >
        </div>
        <div class="form-field">
          <label for="cood">Galactic Coordinates</label>
          <input id="cood" pattern="[0-9]*"  type="number"  inputmode="numeric"  placeholder="Enter space location">
        </div>

        <button class="hvr-sweep-to-left" > Enter Orbit</button>

      </form>

      <router-link to="/" class="back-hm"> <i class="fas fa-chevron-left" style="margin-right: .5rem;"></i> Back Home </router-link>
      
    </div>

  </div>
</template>

<script>
export default {
  name: 'join',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
  @import '../../public/style.css';

  * {
    font-family: 'TT Norms Pro', 'sans-serif';
    box-sizing: border-box;
  }


  .pilot {
    background: url('../assets/img/astro-white.svg');
    height: 100px;
    background-repeat: no-repeat;
    background-size: 12%;
    background-position: 50% 50%;
    animation: bounce 3s infinite;
    animation-timing-function: ease-in-out;
  }

  @keyframes bounce {
    0% {background-position: 50% 50%;}
    50% {background-position: 50% 25%;}
    100% {background-position: 50% 50%;}
  }



.container {
  background-image: url('../assets/img/back-drop.svg');
  background-size: cover;
  color: #fff;
  background-color: #000;
  height: calc(100vh);
  padding: 0 6%;

}
  
  .card {
    width: 40vw;
    height: 60vh;
    /*background-color: #fff;*/
    margin: 0 auto;
    border-radius: 10px;
    padding-top: 10%;

  }

  .card img {
    display: block;
    margin: 0 auto;
  }

  form {
    margin: 0 15%;
  }

  input {
    border-radius: 5px;
    border: 1px solid #fff;
    background-color: transparent;
    width: 100%;
    padding: 1.3rem 1rem;
    color: #fff;
    font-size: 18px;
    transition: all 0.5s ease-in-out;
    /*border: none;*/
  }

  input:focus {
    outline:none;
    border: 1px solid #7842F0;
  }


  .form-field {
    margin: 0 auto;
    display: block;
    margin-bottom: 7%;
  }

  .form-field  label {
    display: block;
    margin-bottom: 10px;
    font-size: 18px;
  }



  button {
    color: #fff;
    letter-spacing: 2px;
    text-decoration: none;
    border: 2px solid #7842F0;
    border-radius: 5px;
    width: 100%;
    padding: 1.4rem 1rem;
    font-weight: 700;
    background-color: #7842F0;
    cursor: pointer;
    margin-top: 1.5rem;
  }


  button:hover {
    /*background-color: #7842F0;*/
    color: #fff;
    font-weight: 900;
    /*font-size: 18px;*/
    text-transform: uppercase;
  }

  ::placeholder {
    font-size: 14px;
    font-weight: 500;
  }

  .back-hm {
    display: block;
    text-align: center;
    margin-top: 2.5rem;
    text-decoration: none;
    color: #FFF;
    font-size: 1.2rem;
  }



  @media only screen and (max-width: 500px) {

    form {
      margin: 0;
    }

    .card {
      width: 80vw;
    }
  }

</style>
