<script>
import ReservationBtn from '../components/ReservationBtn.vue';
import RedirectionBtn from '../components/RedirectionBtn.vue';
import Header from '../components/Header.vue'
import SectionAbout from '../components/AccueilComponent/SectionAbout.vue'
import CardTeam from '../components/AccueilComponent/CardTeam.vue';
import SectionTeam from '../components/AccueilComponent/SectionTeam.vue'
import SectionService from '../components/AccueilComponent/SectionService.vue'
import SectionHome from '../components/AccueilComponent/SectionHome.vue'

import CardService from '../components/AccueilComponent/CardService.vue'
import Carousel from '../components/AccueilComponent/Carousel.vue'
import SectionFooter from '../components/AccueilComponent/SectionFooter.vue'
import InfiniteImg from '../components/AccueilComponent/InfiniteImgCarousel.vue'

export default {
    data() {
        return {

        }
    },
    components: {
        ReservationBtn,
        RedirectionBtn,
        Header,
        SectionAbout,
        CardTeam,
        SectionTeam,
        SectionService,
        SectionHome,

        CardService,
        Carousel,
        SectionFooter,
        InfiniteImg,
    }
    ,methods:{
        allo(){
            
        }
    }
}

</script>

<template>
    <main>

        <!-- <ReservationBtn></ReservationBtn> -->
        <!-- <RedirectionBtn></RedirectionBtn> -->
        <!-- <Header class="stick" id="navbar"></Header> -->
     
       
        <!-- <InfiniteImg></InfiniteImg> -->
        <SectionAbout></SectionAbout>
        <transition
        appear
        @before-appear="">
            <SectionHome></SectionHome>
        </transition>
        <!-- <CardTeam></CardTeam> -->
        <SectionTeam></SectionTeam>
        <!-- <CardService></CardService> -->
        <SectionService></SectionService>
        <!-- <Carousel></Carousel> -->
        <SectionFooter></SectionFooter>



    </main>

</template>
<style scoped>
body,
html {
    margin: 0;
    padding: 0;
    min-height: 100vh;
    max-width: 100vw;
}

main {
    margin: 0;
    padding: 0;
    min-height: 100vh;
    max-width: 100vw;
    display: flex;
    flex-direction: column;
    /* justify-content: center;*/
    align-items: center;
    overflow-x: hidden;

    background-color: #010001;
}
</style>