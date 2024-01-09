<script>
import CardComics from "./CardComics.vue"
export default{
    name: "AppMain",
    components: {
        CardComics
    },
    data(){
      return{
      } 
    }
}
   
</script>
<template lang="">
    <div class="bg-nero">
        <img src="/jumbotron.jpg" alt="" class="jumbo">
        <div class="container">
            <!-- TESTO PLACEHOLDER -->
            <h3><CardComics/></h3>
            
        </div>
    </div>


</template>
<style lang ="scss" scoped>
/* COLORE BACKGROUND */
.bg-nero{
    background-color: black;
    color: white;
    align-items: center;
    

}
.jumbo{
    width:100%;
    height: 300px;
}

</style>