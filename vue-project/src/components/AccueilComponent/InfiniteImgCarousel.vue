<script>
import {gsap,Linear} from 'gsap';
export default{
    data(){
        return{

        }
    },
    methods:{
        infiniteCarousel(){
let titleAbout2 = document.querySelectorAll(".infinite-img-carousel")
console.log('hha')
let carrouselTitle = gsap.timeline()
carrouselTitle.to(titleAbout2,{
    duration : 5,
    x:"-100%",
    repeat:-1,
    ease: Linear.ease
    
})
        }
    }
    ,
    mounted(){
        this.infiniteCarousel()
    }
}
</script>
<template>
    <div class="infinite-carousel-container">
        <div class="infinite-img-carousel">
            <img src="../../assets/academie-service.png" alt="">
        </div>
        <div class="infinite-img-carousel">
            <img src="../../assets/academie-service.png" alt="">
        </div>
        <div class="infinite-img-carousel">
            <img src="../../assets/academie-service.png" alt="">
        </div>
        <div class="infinite-img-carousel">
            <img src="../../assets/academie-service.png" alt="">
        </div>
        <div class="infinite-img-carousel">
            <img src="../../assets/academie-service.png" alt="">
        </div>
        <div class="infinite-img-carousel">
            <img src="../../assets/academie-service.png" alt="">
        </div>

    </div>
</template>
<style>
.infinite-carousel-container{
    position: relative;
    z-index: 5;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    width: 100vw;
    height: 80vh;
}
.infinite-img-carousel{
    padding-right: 1%;
    white-space: nowrap;
    user-select: none;
    color: white;
   }
   .infinite-img-carousel>h1{
    color: white;
   }
   .infinite-img-carousel>img{
    height: 300px;
    height: 200px;
   }

</style>