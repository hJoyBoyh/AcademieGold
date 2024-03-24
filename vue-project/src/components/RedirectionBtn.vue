<script>
export default {
  props: {
    title: String,
  }
}

</script>
<template>
    <div>
        <p>{{title}}</p>
    </div>

</template>
<style scoped>
div{
    height: 50px;
    width: 250px;
    background-color: transparent;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    border: 1px solid white;
    border-radius: 30px;
    cursor: pointer;
    transition: 0.3s;
}
p{
    margin: 0;
    padding: 0;
    font-size: 24px;
    font-weight: 700;
   
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}
div:hover{
    background-color: #CFA246;
    border: 1px solid #CFA246;
        color: #111111;
}
</style>