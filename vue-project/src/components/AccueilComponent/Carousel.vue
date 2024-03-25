
<script>
import CardService from './CardService.vue'


export default {
    data() {
        return {};
    },
    components:{
        CardService,
       
    },
}

</script>
<template>
    <h1>NETFLIX</h1>
    <div class="carousel-container">
<div class="wrapper">
  <section id="section1">
    <a href="#section3" class="arrow__btn">‹</a>
    <div class="item">
        <CardService></CardService>
  </div>
    <div class="item">
        <CardService></CardService>  </div>
    <div class="item">
        <CardService></CardService>  </div>
    <div class="item">
        <CardService></CardService>  </div>
    <div class="item">
        <CardService></CardService>  </div>
    <a href="#section2" class="arrow__btn">›</a>
  </section>
  <section id="section2">
    <a href="#section1" class="arrow__btn">‹</a>
    <div class="item">
        <CardService></CardService>  </div>
    <div class="item">
        <CardService></CardService>  </div>
    <div class="item">
        <CardService></CardService>  </div>
    <div class="item">
        <CardService></CardService>  </div>
    <div class="item">
        <CardService></CardService>  </div>
    <a href="#section1" class="arrow__btn">›</a>
  </section>
  <!-- <section id="section3">
    <a href="#section2" class="arrow__btn">‹</a>
    <div class="item">
    <img src="https://occ-0-243-299.1.nflxso.net/dnm/api/v5/rendition/412e4119fb212e3ca9f1add558e2e7fed42f8fb4/AAAABRr4YxdaABuAuH_3FmSQZn7BCvLp-UUPsXE9MiYpvFP3CSUHV2zOew5oVqKqqdaOd3tbFVS0Uf67uIs7_eZydlCghg4nK0nMatRpPImABwTOhnNzCLCxdKrua7pPIcPCZqBYTeAO5g.jpg" alt="Describe Image">
  </div>
    <div class="item">
    <img src="https://occ-0-243-299.1.nflxso.net/dnm/api/v5/rendition/412e4119fb212e3ca9f1add558e2e7fed42f8fb4/AAAABTyWK1MKaw8GcObtz47R2Tj7wkLJ7qQu9tk6TVpcoyxpzD4B-zZ569bQ5vGrREBL-MWFkGilXUwy7tCDaj2XOGkUB4RsbbFAmp9NgSr6lygMpUGNHSlyfrFbUORsRkrxSIoh_ggOvg.jpg" alt="Describe Image">
  </div>
    <div class="item">
    <img src="https://occ-0-243-299.1.nflxso.net/dnm/api/v5/rendition/a76057bcfd003711a76fb3985b1f2cf74beee3b8/AAAABY7NwkWEJIfXsn6t3Li4bGSCQ1nEErPisI5ZZtXlC-_VRBZOUrhWK5X3vt3t6SR_cpgVhCwxgQqFFDJhk62Kk8hawOnYGZMr0LKeLczMFV2zalCFjkcdLksvT4HB2LEi6LFyruyk3Uu0LmNGsHfC2A8Bly60smr_3sDbz4RruXcklPOG1qYq9wUVu3zfaiwNvqmG4b8aFA.jpg" alt="Describe Image">
  </div>
    <div class="item">
    <img src="https://occ-0-243-299.1.nflxso.net/dnm/api/v5/rendition/a76057bcfd003711a76fb3985b1f2cf74beee3b8/AAAABemXHOga9feFnOux6I2YyACBD94wvM7N3vcTGIfMpQ_BcaXeoeM9XyzdVdamKtxt0SHXZfvsl6czcp3E48tXMLtHBxuQsh1BjHtPGgJDZ81je_FjItINiqzLtir0A30s_e4KR8G3d7AYAPDjZVOY97bNpzNqtkcHcGp7fGnJByVCps1uLfG9U9tK3Ma1A_3JbRt0NiT2_Q.jpg" alt="Describe Image">
  </div>
    <div class="item">
    <img src="https://occ-0-243-299.1.nflxso.net/dnm/api/v5/rendition/a76057bcfd003711a76fb3985b1f2cf74beee3b8/AAAABVxuRB932hvre-XP0gh6ar5ztoR3Oe3QjKHkyvcDnRak2MKXOrx5H7mFQSvggefMFOppwEs7ZCCpiqrJ_CYGvtvYB9NpU4SWUtNO6uV2u-DTID267AcHjHcGvGBQJ1ufddDkxcGOZyi5MlOQ5QUmBun4652FbYUnib3zMYQDgcna_Pvz8y_HO5fbokxezrRR1JZAAiqFSQ.jpg" alt="Describe Image">
  </div>
    <a href="#section1" class="arrow__btn">›</a>
  </section> -->
</div>
</div>



</template>
<style>
html {
    scroll-behavior: smooth;
}
body {
    margin: 0;
    background-color: #000;
}
h1 {
    font-family: Arial;
 
    text-align: center;
}
.carousel-container{
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
}
.wrapper {
    display: grid;
    grid-template-columns: repeat(3, 100%);
    overflow: hidden;
    scroll-behavior: smooth;
    width: 70%
}
.wrapper section {
    height: 70vh;
    width: 100%;
    position: relative;
    display: grid;
    grid-template-columns: repeat(5, auto);
    margin: 20px 0;
}
.wrapper section .item {
    padding: 0 2px;
    transition: 250ms all;
}
.wrapper section .item:hover {
    margin: 0 40px;
    transform: scale(1.2);
}
.wrapper section a {
    position: absolute;
    color: #fff;
    text-decoration: none;
    font-size: 6em;
    background: #000;
    width: 80px;
    padding: 20px;
    text-align: center;
    z-index: 1;
}
.wrapper section a:nth-of-type(1) {
    top: 0;
    bottom: 0;
    left: 0;
}
.wrapper section a:nth-of-type(2) {
    top: 0;
    bottom: 0;
    right: 0;
    background: linear-gradient(90deg, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 1) 100%);
}
@media only screen and (max-width: 600px) {
    a.arrow__btn {
        display: none;
   }
}

</style>