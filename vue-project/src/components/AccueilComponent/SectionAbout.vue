<script>
import RedirectionBtn from '../RedirectionBtn.vue'
import { gsap } from 'gsap'

export default {
    data() {
        return {};
    },
    components: {
        RedirectionBtn,
    },
    methods:{
        sectionAboutAnimation(){
            let tl = gsap.timeline()
            tl.from('.about-container>p>span',{
                duration:0.5,
                opacity:0,
                stagger:0.1
            })
            tl.from('.btn-container',{
                duration:0.2,
                opacity:0
            })
        }
    },
    mounted(){
        this.sectionAboutAnimation()
    }
}
</script>
<template>
    <div class="about-container">
        <p>

            <span>Eindhoven </span>
            <span>Design </span>
            <span>District </span>
            <span>is </span>
            <span>een </span>
            <span>initiatief </span>
            <span>van </span>
            <span>gemeente </span>
            <span>Eindhoven </span>
            <span>, Dutch </span>
            <span>Design </span>
            <span>Foundation </span>
            <span>en </span>
            <span>Eindhoven365 </span>
            <span>om </span>
            <span>design </span>
            <span>en </span>
            <span>technologie </span>
            <span>in </span>
            <span>Eindhoven </span>
            <span>een </span>
            <span>groter </span>
            <span>podium </span>
            <span>te </span>
            <span>bieden </span>
            <span>en </span>
            <span>design </span>
            <span>thinking </span>
            <span>te </span>
            <span>stimuleren </span>
            <span>bij </span>
            <span>bedrijven </span>
            <span>en </span>
            <span>overheden. </span>
            <span>Op </span>
            <span>deze </span>
            <span>website </span>
            <span>vind </span>
            <span>je </span>
            <span>informatie </span>
            <span>over </span>
            <span>de.</span>

        </p>

        <div class="btn-container">
        <RedirectionBtn class="btn" title="About"></RedirectionBtn>
    </div>
    </div>

</template>
<style scoped>
.about-container {
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

.about-container {

    width: 90%;
}

.about-container>p {
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;

}
.about-container>p>span{
    opacity:1
}
.btn-container{
    opacity: 1;
}
</style>