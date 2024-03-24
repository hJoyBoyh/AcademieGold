<script>
import CardService from './CardService.vue'
import RedirectionBtn from '../RedirectionBtn.vue'


export default {
    data() {
        return {};
    },
    components:{
        CardService,
        RedirectionBtn
       
    },
}
</script>
<template>
    <div class="services-container">
        <div class="services-title-container">
            <h2>Nos Services</h2>
        </div>
        <div class="services-content">
            <CardService></CardService>
            <CardService></CardService>
            <CardService></CardService>



        </div>
        <div class="redirection-btn-container">
        <RedirectionBtn title="Voir plus"></RedirectionBtn>
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
</style>