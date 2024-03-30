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
            document.querySelector('.home-first-section').style.opacity = 0
            document.querySelector('.home-second-section').style.opacity = 0
            document.querySelector('.home-third-section').style.opacity = 0


            setTimeout(() => {
                
                document.querySelector('.home-first-section').style.opacity = 1
            document.querySelector('.home-second-section').style.opacity = 1
            document.querySelector('.home-third-section').style.opacity = 1

            
            // if(StartAnimation === true){
            let tl = gsap.timeline()
            let tl2 = gsap.timeline()
            tl2.add('start')
            tl.add('start')

           

            tl.to('.home-third-section>p', {
                duration: 1,
                opacity:1,
                transformOrigin:'left center',
                ease: "power4.out"
            }, )
            

            tl.from('.home-first-section>h1>span', {
                duration: 0.5,
                y: -350,
                stagger: 0.1,
                ease: "power4.out"
            }, )

            tl.from('.home-second-section-title>h1>span', {
                duration: 0.7,
                y: -350,
                stagger: 0.1,
                ease: "power4.out",
                delay:-0.7
            
            },)


            tl.from('.home-third-section-title>h1>span', {
                duration: 0.7,
                y: -350,
                stagger: 0.1,
                ease: "power4.out",
                delay:-0.7
            },)

    tl.from('.home-img-1-container', {
                duration: 3,
                transformOrigin: 'top center',
                scaleY: 0,
                ease: "power4.out",
                delay:2.2
            }, 'start')
            tl.from('.home-img-1', {
                duration: 1,
                transformOrigin: 'center center',
                scale: 7,
                ease: "circ.out",
                delay:2.2
            }, 'start')

            tl.from('.home-img-2-container', {
                duration: 3,
                transformOrigin: 'left center',
                scaleX: 0,
                ease: "power4.out",
                delay:2.2
            }, 'start')
            tl.from('.home-img-2', {
                duration: 1,
                transformOrigin: 'center center',
                scale: 7,
                ease: "circ.out",
                delay:2.2
            }, 'start')


            


            
        // }
    }, 9000);
        }
        
    }
    ,
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
    align-items: center;
    height: 100vh;
    width: 100vw;

    background-color: black;
    color: white;
      font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

}

.home-first-section>h1 {
    margin: 0;
    font-size: 7em;
    width: 90vw;
    display: flex;
    justify-content: flex-start;
    align-items: baseline;
    position: relative;
    left: 50px;
    overflow: hidden;
}

.home-second-section-title>h1 {
    margin: 0;
    font-size: 7em;
    display: flex;
    justify-content: flex-start;
    align-items: baseline;
    overflow: hidden;
    transform: rotate(-90deg);
    position: relative;
    top: 95px;
  
    color: #CFA246;
}

.home-third-section-title>h1 {
    margin: 0;
    font-size: 7em;
    display: flex;
    justify-content: flex-start;
    align-items: baseline;
    overflow: hidden;
    position: relative;
    bottom: 80px;
    right: 140px;

}


.home-second-section {
    display: flex;
    width: 90vw;
    justify-content: space-between;

}

.home-img-1-container {
    height: 270px;
    overflow: hidden;
    position: relative;
    left:60px;
    top:20px

   
}

.home-img-1 {
    height: 100%;


}

.home-second-section>h1 {
    font-size: 7em;
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
    font-size: 7em;
    margin: 0;
    position: relative;
    bottom: 100px;
    overflow: hidden;

}

.home-third-section>p {
    font-size: 1.5em;
    width: 20%;
    position: relative;
    bottom: 50px;
    left:50px;
    opacity: 0;
}
</style>