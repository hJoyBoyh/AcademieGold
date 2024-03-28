<script>
import CardService from './CardService.vue'
import RedirectionBtn from '../RedirectionBtn.vue'
import {gsap} from 'gsap'


export default {
    data() {
        return {};
    },
    components:{
        CardService,
        RedirectionBtn
       

    },
    methods:{
        sectionServiceAnimation(){
            let tl = gsap.timeline();
            tl.from('.services-title-container',{
                duration:1,
                x:-150,
                opacity:0
            })
            tl.from('.card-service',{
                duration:1,
                y:150,
                opacity:0,
                stagger:0.2

            })
            tl.to('.btn-service',{
                duration:0.3,
                opacity:1,
                

            })
        }
    },
    mounted(){
        this.sectionServiceAnimation()
    }
}
</script>
<template>
    <div class="services-container">
        <div class="services-title-container">
            <h2>Nos Services</h2>
        </div>
        <div class="services-content">
            <CardService class="card-service"</CardService>
            <CardService class="card-service"</CardService>
            <CardService class="card-service"></CardService>



        </div>
        <div class="redirection-btn-container">
        <RedirectionBtn title="Voir plus" class="btn-service"></RedirectionBtn>
    </div>
    </div>

</template>
<style scoped>
.services-container{
    color: white;
    
    max-width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    /*give more space bew*/
    padding-bottom: 20vh;
    


}
.services-title-container>h2{
    font-size: 3em;
    margin: 0;
    padding: 0;
    margin-left: 5vw;
}
.services-content{
    min-height: 60vh;
    width: 100vw;
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.redirection-btn-container{
    
    height: 30vh;
    margin-top: 10vh;
    margin-left: 10vh;
    
    display: flex;
    justify-content: flex-start;
    align-items: center;
}
.card-service{
    opacity: 1;
}
.btn-service{
    opacity: 0;
}
</style>