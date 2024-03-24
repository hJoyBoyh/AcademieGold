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
 <footer>
    <div class="footer-title">
        <h1>Alors intéresser <span>?</span></h1>
    </div>


 </footer>

</template>
<style scoped>
span{
    color: #CFA246;
}
.footer-title{
    height: 50vh;
    color: white;
}
.footer-title>h1{
    font-size: 5em;
    color: white;
}
</style>