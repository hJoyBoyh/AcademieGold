<script>
import ReservationBtnWhite from './ReservationBtnWhite.vue'

export default {
    data() {
        return {};
    },
    components: {
        ReservationBtnWhite,

    },
    methods: {
        showNavBar() {
            var prevScrollpos = window.scrollY;
            window.onscroll = function () {
                var currentScrollPos = window.scrollY;
                if (prevScrollpos > currentScrollPos) {
                    document.getElementById("navbar").style.top = "0";
                } else {
                    document.getElementById("navbar").style.top = "-50px";
                }
                prevScrollpos = currentScrollPos;
            }
        },
        menuBurger() {
            let x = document.querySelector('.burger-container')
            x.classList.toggle("change");


        }
    },
    mounted() {
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
        <!-- <li class="hover-underline-animation">Accueil</li>
        <li class="hover-underline-animation">Service</li>
        <li class="hover-underline-animation">Porfolio</li> -->
                <ReservationBtn></ReservationBtn>
                <div class="burger-container" @click="menuBurger">
                    <div class="bar1"></div>
                    <div class="bar2"></div>
                    <div class="bar3"></div>
                </div>




            </div>

        </div>
        <div class="show-menu">
            <div class="menu-container">
                <div class="menu-option-container">
                    <a href="">  
                        <li class="hover-underline-animation">Accueil</li>
                    </a>
                    <a href="">
                        <li class="hover-underline-animation" >Porfolio</li>
                    </a>
                    <a href="">
                        <li class="hover-underline-animation">Service</li>
                    </a>
                </div>
                <div class="contact-option-container">
                    <div class="social-menu">
                        <h2>Social</h2>
                        <a href="">
                            <li class="hover-underline-animation">Instagram</li>
                        </a>
                        <a href="">
                            <li class="hover-underline-animation">Facebook</li>
                        </a>


                    </div>
                    <div class="social-menu">
                        <h2>Ou nous trouver</h2>
                        <a href="">
                            <p class="hover-underline-animation">9468 rue Hochelaga, Montréal,QC</p>
                        </a>
                        

                    </div>
                </div>
            </div>

            <ReservationBtnWhite></ReservationBtnWhite>
        </div>
    </header>

</template>
<style scoped>
header {
    width: 100vw;
    height: 22vh;
    position: sticky;
}

.header-container {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;

}

.logo-container {
    height: 150px;
    overflow: hidden;
}

img {
    height: 300px;
    position: relative;
    bottom: 90px
}

.nav-container {
    position: relative;

    color: white;
    width: 23%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 50px;
}

li {
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    list-style-type: none;
    cursor: pointer;
    

}

.burger-container {
    display: inline-block;
    cursor: pointer;
    position: relative;
    z-index: 200;
}

.bar1,
.bar2,
.bar3 {
    width: 45px;
    height: 2px;
    background-color: white;
    margin: 5px 0;
    transition: 0.4s;
}

.change .bar1 {
    transform: translate(0, 11px) rotate(-45deg);
}

.change .bar2 {
    opacity: 0;
}

.change .bar3 {
    transform: translate(0, -11px) rotate(45deg);
}

.show-menu {
    width: 60vw;
    height: 100vh;
    background-color: #CFA246;
    position: fixed;
    z-index: 100;
    top: 0;
    right: 0;
    display: flex;

    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
}
.menu-container{
    height: 80%;
    width:80%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
.menu-option-container{
    line-height: 1.5;
    display: flex;
    flex-direction: column;
}
.menu-option-container>a:nth-child(1){
    color: white

}
.menu-option-container>a{
    text-decoration: none;
    color: #d9c49b

}
.menu-option-container>a>li{
    font-size: 4em;
    
}

.social-menu {
    display: flex;
    flex-direction: column;
    line-height: 2;
}
.social-menu>h2{
    color: #d9c49b;
    margin: 0;
} .social-menu>a>p{
    margin: 0;
    color: white
}
.social-menu>a>li{
    margin: 0;
    color: white
}
.contact-option-container{
    height: 40vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between
}




.hover-underline-animation {
    display: inline-block;
    position: relative;
  /*  color: white;*/
}

.hover-underline-animation::after {
    content: '';
    position: absolute;
    width: 100%;
    transform: scaleX(0);
    height: 3px;
    bottom: 0px;
    left: 0;
    background-color: white;
    color: white;
    transform-origin: bottom right;
    transition: transform 0.25s ease-out;
}

.hover-underline-animation:hover::after {
    transform: scaleX(1);
    transform-origin: bottom left;
}
</style>