<script>
import RedirectionBtn from '../RedirectionBtn.vue'

export default {
    data() {
        return {};
    },
    components:{
        RedirectionBtn,
       
    },
}
</script>
<template>
    <div class="about-container">
       <p>Eindhoven Design District is een initiatief van gemeente Eindhoven, Dutch Design Foundation en Eindhoven365 om design en technologie in Eindhoven een groter podium te bieden en design thinking te stimuleren bij bedrijven en overheden. Op deze website vind je informatie over de projecten die wij realiseren en best-practices uit het Eindhovense ontwerpveld.</p>
        <RedirectionBtn class="btn" title="About"></RedirectionBtn>
    </div>

</template>
<style scoped>
.about-container{
    color: white;
    font-size: 2em;
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    /*give more space bew*/
    padding-bottom: 20vh;


}
.about-container{
   
    width: 90%;
}
.about-container>p{
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

}

</style>