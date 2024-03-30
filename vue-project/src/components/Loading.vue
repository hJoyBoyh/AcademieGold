<script>
import {gsap} from 'gsap';
import SectionHome from './AccueilComponent/SectionHome.vue'
import SectionAbout from './AccueilComponent/SectionAbout.vue'

export default{
    data(){
        return{

        }
    },
    components:{
        SectionHome,
        SectionAbout
    },
    methods:{
        loaderAnimation(){
            function startLoader(){
    let counterElement = document.querySelector(".counter")

    let currentValue = 0
    function updateCounter(){
        if(currentValue === 100){
            return;
        }
        currentValue += Math.floor(Math.random()*10) +1;
        if(currentValue > 100){
            currentValue = 100
        }
        counterElement.textContent = currentValue + "%";
        let delay = Math.floor(Math.random()*200)+250;
        setTimeout(updateCounter,delay)
    }
    updateCounter()
   
}
startLoader()

gsap.from('.circles',2,{
    top:"-100%",
    ease:"elastic.out",
    delay:0.5
})
gsap.to('.circle-inner',1,{
    width:"75px",
    height:"75px",
    ease:"power4.inOut",
    delay:2
})
gsap.to('.circle-inner-rotator',1,{
    scale:1,
    ease:'power4.inOut',
    delay:2.5,

})

gsap.to('.circles',1.5,{
    rotation:360,
    ease:'power4.inOut',
    delay:3,
})

gsap.to('.block',0.75,{
   display:'block',
   height:'200px',
    ease:'power4.inOut',
    delay:4,
})
gsap.to('.block',0.75,{
    display:'block',
    width:'800px',
     ease:'power4.inOut',
     delay:4.5,
 })

 gsap.fromTo('.container',{
    duration:2,
    left:'100%',
    scale:0.5,
    ease:'power4.inOut',
    delay:4
 },{
    duration:2,
    left:'50%',
    scale:0.5,
    transform:'translateX(-50%)',
    ease:'power4.inOut',
    delay:4
 })
 gsap.to('.block',1.5,{
    width:'0px',
    ease:'power4.inOut',
    delay:5
 })
 gsap.to('.block',1.5,{
    height:'0px',
    ease:'power4.inOut',
    delay:6
 })
 gsap.to('.circles',1.5,{
    rotation:0,
    ease:'power4.inOut',
    delay:6.5,
})
gsap.to('.loader',2.5,{
    scale:0,
    ease:'power4.inOut',
    delay:7
})
gsap.to('.container',2,{
    scale:1,
    ease:'power4.inOut',
    delay:7.5,
})
        }
    },
    mounted(){
        this.loaderAnimation()
    }
}
</script>
<template>
    <div class="loader">
        <h1 class="counter">0</h1>
        <div class="site-teaser">
            <!-- <span>Use headphone for better experience</span> -->
        </div>
        <div class="circles">
            <div class="circle circle-outer"></div>
            <div class="circle circle-inner"></div>
            <div class="circle-inner-rotator"></div>
            <div class="block"></div>
        </div>
    </div>
   
        <!-- <h1>H <span>i</span></h1> -->
        <div class="container">
            <SectionHome ></SectionHome>
        </div>
      


</template>
<style scoped>
:root{
    --circle-outline: #505050
}
*{
    margin:0;
    padding: 0;
    box-sizing: border-box;
}
html,body{
   min-width:100vw ;
    min-height: 100vh;
    
   /* background: #181818;*/
   font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

}
.loader{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
   /* background: #000;*/
}
.counter{
    width: 100%;
    height: 100%;
    position: fixed;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    color: var(--circle-outline);
    padding: 2rem 4rem;
    font-size: 10vw;
    font-family: "Saol Display";
    font-weight: lighter;
    font-style: italic;
    z-index: 1000;
}
.site-teaser span{
    position: absolute;
    top: 0;
    right: 0;
    padding:2rem 4rem;
    color: var(--circle-outline);
    font-size: 1rem;
    font-family: "Saol Display";
    font-weight: lighter;
    font-style: italic;

}

.circles{
    position: absolute;
    left: 5rem;
    bottom: 5rem;
    width: 400px;
    height: 400px;
    border-radius: 100%;
}
.circle{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: none;
    border: 1px solid var(--circle-outline);
    border-radius: 100%;
}
.circle-inner{
    position: absolute;
   top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 400px;
    height: 400px;
}
.circle-inner-rotator{
    position: absolute;
    left: 50%;
    transform:  translateX(-50%) scale(0);
    width: 162.5px;
    height: 162.5px;
    background: none;
    border: 1px solid var(--circle-outline);
    border-radius: 100%;


}
.block{
    position: absolute;
    top: -100px;
    left: 200px;
    width: 0px;
    height: 0px;
    display: none;
    background: none;
    border: 1px solid var(--circle-outline);
transform-origin: bottom;
}
.container{
    position: fixed;
    top: 0;
    left: 0;
    background-color: #131313
   
   
}


</style>