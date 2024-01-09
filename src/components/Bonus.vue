<script>
export default{
    name: "Bonus",
    data(){
      return{
        bonus:[
            {
                icon_buy: "/buy-comics-digital-comics.png",
                testo: "DIGITAL COMICS"
            },
            {
                icon_buy: "/buy-comics-merchandise.png",
                testo: "DC MERCHANDISE"
            },
            {
                icon_buy: "/buy-comics-subscriptions.png",
                testo: "SUBSCRIPTION"
            },
            {
                icon_buy: "/buy-comics-shop-locator.png",
                testo: "COMIC SHOP LOCATOR"
            },
            {
                icon_buy: "/buy-dc-power-visa.svg",
                testo: "DC POWER VISA"
            },
        ]
      }
    }
}
</script>
<template lang="">
  <div>
<!-- SFONDO BONUS -->
<div class="sfondo-bonus">
        <!-- CONTAINER -->
        <div class="container">
            <div class="d-flex mx-4" >
                <!-- LISTA BONUS CON V-FOR PER TESTO E IMMAGINE -->
                <ul> 
                    <li v-for= "(icon ,index) in bonus" :key="index" ><a href=""><img class="mx-3" :src="icon.icon_buy" alt="icon-social" ></a>
                        <a href="">{{ icon.testo }}</a></li>
                </ul>
            </div>        
        </div>
    </div>
  </div>
</template>
<style lang ="scss" scoped>
/* STILE SFONDO BONUS */
@use "../styles/partials/variables" as *;
.sfondo-bonus{
    background-color: $primary_color;
    /* STILE DI A, UL, LI, IMG E HOVER DELL'IMMAGINE ALL'INTENRO DEL BONUS */
    a{
        color: white
    }
    ul{
        display: flex;
        flex-direction: row;
        align-items:center;
        padding: 30px 0px;
        margin: 0;
    }
    li{
        margin: 10px;
        list-style-type: none;
    }
    img{
        width: 40px
    }
    img:hover{
        width: 55px;
        transition: 0.5s;
        
    }
}
</style>