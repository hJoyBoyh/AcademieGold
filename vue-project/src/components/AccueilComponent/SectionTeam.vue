<script>
import CardTeam from './CardTeam.vue'
import { gsap } from 'gsap'




export default {
    data() {
        return {};
    },
    components:{
        CardTeam, 
    },
    methods:{
        sectionTeamAnimation(){
            let tl = gsap.timeline();
            tl.from('.team-title-container',{
                duration:1,
                x:-150,
                opacity:0
            })
            tl.from('.card',{
                duration:1,
                y:150,
                opacity:0,
                stagger:0.2

            })

        }
    },
    mounted(){
        this.sectionTeamAnimation()
    }
}
</script>
<template>
    <div class="team-container">
        <div class="team-title-container">
            <h2>Notre Equipe</h2>
        </div>
        <div class="team-content">
            <CardTeam  class="card"></CardTeam>
            <CardTeam class="card"></CardTeam>


        </div>
      
    </div>

</template>
<style scoped>
.team-container{
    color: white;
    
    max-width: 100vw;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    /*give more space bew*/
    padding-bottom: 20vh;


}
.team-title-container{
    opacity: 1;
}
.team-title-container>h2{
    font-size: 3em;
    margin: 0;
    padding: 0;
    margin-left: 5vw;
}
.team-content{
    height: 80vh;
    width: 100vw;
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.card{
    opacity: 1;
}
</style>