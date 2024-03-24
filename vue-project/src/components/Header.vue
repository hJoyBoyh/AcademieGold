<script>
import ReservationBtn from './ReservationBtn.vue'

export default {
    data() {
        return {};
    },
    components:{
        ReservationBtn,
       
    },
    methods:{
        showNavBar(){
            var prevScrollpos = window.scrollY;
window.onscroll = function() {
  var currentScrollPos = window.scrollY;
  if (prevScrollpos > currentScrollPos) {
    document.getElementById("navbar").style.top = "0";
  } else {
    document.getElementById("navbar").style.top = "-50px";
  }
  prevScrollpos = currentScrollPos;
}
        }
    },
    mounted(){
        this.showNavBar()
    }
}
</script>
<template>
    <header>
    <div class="header-container" id="navbar">
       <div class="logo-container">
        <img src="../assets/academie-black-logo.jpg" alt="">
       </div>
       <div class="nav-container">
        <li class="hover-underline-animation">Accueil</li>
        <li class="hover-underline-animation">Service</li>
        <li class="hover-underline-animation">Porfolio</li>
        <ReservationBtn></ReservationBtn>
        



       </div>
    </div>
</header>

</template>
<style scoped>

header{
    width: 100vw;
    height: 22vh;
    position: sticky;
}
.header-container{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    
}
.logo-container{
    height: 150px;
    overflow: hidden;
}
img{
    height: 300px;
    position: relative;
    bottom:90px
}
.nav-container{
    position: relative;
    
    color: white;
    width: 50%;
    height: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
}
li{
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
list-style-type: none;
cursor: pointer;

}
.hover-underline-animation {
    display: inline-block;
    position: relative;
    color: white;
  }
  
  .hover-underline-animation::after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(0);
    height: 2px;
    bottom: 0;
    left: 0;
    background-color:#CFA246;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
  }
  
  .hover-underline-animation:hover::after {
    transform: scaleX(1);
    transform-origin: bottom left;
  }

</style>