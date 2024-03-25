<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);



export default {
    data() {
        return {

        }
    },
    props:{
        StartAnimation:Boolean
    },
    methods: {
        test() {
            if(StartAnimation === true){
            let tl = gsap.timeline()
            tl.add('start')

            tl.from('.home-img-1-container', {
                duration: 2,
                transformOrigin: 'top center',
                scaleY: 0,
                ease: "power4.out",
            }, 'start')
            tl.from('.home-img-1', {
                duration: 1,
                transformOrigin: 'center center',
                scale: 5,
                ease: "circ.out",
            }, 'start')

            tl.from('.home-img-2-container', {
                duration: 2,
                transformOrigin: 'left center',
                scaleX: 0,
                ease: "power4.out",
            }, 'start')
            tl.from('.home-img-2', {
                duration: 1,
                transformOrigin: 'center center',
                scale: 5,
                ease: "circ.out",
            }, 'start')


            tl.from('.home-first-section>h1>span', {
                duration: 1,
                y: -350,
                stagger: 0.1,
                ease: "power4.out"
            }, "start")

            tl.from('.home-second-section-title>h1>span', {
                duration: 1,
                y: -350,
                stagger: 0.1,
                ease: "power4.out"
            }, "start")


            tl.from('.home-third-section-title>h1>span', {
                duration: 1,
                y: -350,
                stagger: 0.1,
                ease: "power4.out"
            }, "start")


            
        }
        }
    },
    mounted() {
        this.test()
    }
}
</script>
<template>
    <div class="home-container">
        <div class="home-first-section">
            <h1><span>A</span>
                <span>C</span>
                <span>A</span>
                <span>D</span>
                <span>E</span>
                <span>M</span>
                <span>I</span>
                <span>E</span>
            </h1>
        </div>
        <div class="home-second-section">
            <div class="home-img-1-container">
                <img src="../../assets/accueil-img-1-academie-gold.png" class="home-img-1" alt="" srcset="">
            </div>
            <div class="home-second-section-title">
                <h1><span>G</span>
                    <span>O</span>
                    <span>L</span>
                    <span>D</span>
                </h1>
            </div>
            <div class="home-img-2-container">
                <img src="../../assets/accueil-img-2-academie-gold.png" class="home-img-2" alt="" srcset="">

            </div>

        </div>
        <div class="home-third-section">
            <p>Beauty salon in Montreal</p>
            <div class="home-third-section-title">
                <h1><span>S</span>
                    <span>T</span>
                    <span>U</span>
                    <span>D</span>
                    <span>I</span>

                    <span>O</span>

                </h1>
            </div>


        </div>

    </div>

</template>
<style scoped>
.home-container {
    display: flex;
    flex-direction: column;

}

.home-first-section>h1 {
    margin: 0;
    font-size: 7.5em;
    width: 90vw;
    display: flex;
    justify-content: flex-start;
    align-items: baseline;
    overflow: hidden;
}

.home-second-section-title>h1 {
    margin: 0;
    font-size: 7.5em;
    display: flex;
    justify-content: flex-start;
    align-items: baseline;
    overflow: hidden;
    transform: rotate(-90deg);
    position: relative;
    top: 80px;
    right: 30px;
    color: #CFA246;
}

.home-third-section-title>h1 {
    margin: 0;
    font-size: 7.5em;
    display: flex;
    justify-content: flex-start;
    align-items: baseline;
    overflow: hidden;
    position: relative;
    bottom: 80px;

}


.home-second-section {
    display: flex;
    width: 90vw;
    justify-content: space-between;

}

.home-img-1-container {
    height: 300px;
    overflow: hidden;
}

.home-img-1 {
    height: 100%;


}

.home-second-section>h1 {
    font-size: 7.5em;
    width: 0;
    transform: rotate(-90deg);
    margin: 0;
    margin-bottom: 100px;
    margin-left: 100px;
    overflow: hidden;
    width: 30%;


    color: #CFA246;

}

.home-img-2-container {
    height: 400px;
    position: relative;
    right: 100px;
    bottom: 110px;
    overflow: hidden;
}

.home-img-2 {
    height: 100%;



}

.home-third-section {
    width: 88.5%;
    display: flex;
    justify-content: space-between;

}

.home-third-section>h1 {
    font-size: 7.5em;
    margin: 0;
    position: relative;
    bottom: 100px;
    overflow: hidden;

}

.home-third-section>p {
    font-size: 1.5em;
    width: 20%;
    position: relative;
    bottom: 100px;
}
</style>