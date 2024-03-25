<script>
import {gsap,Linear} from 'gsap';
export default{
    data(){
        return{

        }
    },
    methods:{
        infiniteCarousel(){
// let titleAbout2 = document.querySelectorAll(".infinite-img-carousel")
// console.log('hha')
// let carrouselTitle = gsap.timeline()
// carrouselTitle.to(titleAbout2,{
//     duration : 5,
//     x:"-100%",
//     repeat:-1,
//     ease: Linear.ease
    
// })
        }
    }
    ,
    mounted(){
        this.infiniteCarousel()
    }
}
</script>
<template>
    <section>
    <article>
        <div>
          <ul>
            <li><img src="../../assets/academie-service.png" /></li>
            <li><img src="../../assets/academie-service.png" /></li>
            <li><img src="../../assets/academie-service.png" /></li>
            <li><img src="../../assets/academie-service.png" /></li>
          </ul>
        </div>
        <div>
          <ul>
            <li><img src="../../assets/academie-service.png" /></li>
            <li><img src="../../assets/academie-service.png" /></li>
            <li><img src="../../assets/academie-service.png" /></li>
            <li><img src="../../assets/academie-service.png" /></li>
          </ul>
        </div>
      </article>
    </section>
    <!-- <div class="infinite-carousel-container">
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

    </div> -->
</template>
<style scoped>
img {
    display: block;
    width: 100%;
    transform: rotate(-2deg);
  }
  
  section {
    width: 100%;
  }
  
  article {
    display: flex;
    width: 200%;
    animation: bannermove 20s linear infinite;
    gap:-2px;
  }
  
  article.paused {
    -webkit-animation-play-state: paused;
    animation-play-state: paused;
  }
  
  div {
    width: 100%;
   
  }
  
  ul {
    display: flex;
    gap:-5px;

    list-style-type: none;
    padding-left: 0;
    margin: 0;
  
  }
  
  li {
    width: 100%;
  }
  
  li:nth-child(2) {
  }
  
  li:nth-child(3) {
  }
  
  @keyframes bannermove {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-50%);
    }
  }
/*
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
   }*/

</style>