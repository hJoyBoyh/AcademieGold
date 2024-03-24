<script>
import CardTeam from './CardTeam.vue'

export default {
    data() {
        return {};
    },
    components:{
        CardTeam,
       
    },
}
</script>
<template>
    <div class="team-container">
        <div class="team-title-container">
            <h2>Notre Equipe</h2>
        </div>
        <div class="team-content">
            <CardTeam></CardTeam>
            <CardTeam></CardTeam>


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
</style>