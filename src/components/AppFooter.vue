<script>
export default{
    name: "AppFooter",
    data(){
      return{
        /* ARRAY LISTE FOOTER */
        comics: [
            {
                label: "Character",
                link_utili: "Terms Of Use",
                site: "DC",
                shop: "Shop DC"
            },
            {
                label: "Comics",
                link_utili: "Privacy policy(New)",
                site: "MAD Magazine",
                shop: "Shop DC Collectibles"
            },
            {
                label: "Movies",
                link_utili: "Ad Choices",
                site: "DC Kids"
            },
            {
                label: "TV",
                link_utili: "Advertising",
                site: "DC Universe",
            },
            {
                label: "Games",
                link_utili: "Jobs",
                site: "DC Power Visa",
            },
            {
                label: "Videos",
                link_utili: "Subscriptions"
            },
            {
                label: "News",
                link_utili: "Talent Workshops"
            },
            {
                link_utili: " CPSC Certificates"
            },
            {
                link_utili: "Ratings"
            },
            {
                link_utili: "Shop Help"
            },
            {
                link_utili: "Contact Us"
            },
        ],
        /* ARRAY ICONE SOCIAL */
        social:[
            {
                icon: "/footer-facebook.png"
            },
            {
                icon: "/footer-periscope.png"
            },
            {
                icon: "/footer-pinterest.png"
            },
            {
                icon: "/footer-twitter.png"
            },
            {
                icon: "/footer-youtube.png"
            }
        ],
        /* ARRAY BONUS */
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
    <!-- FOOTER CON IMG DI BACKGROUND -->
    <div class="img-sfondo ">
        <div class="container">
            <!-- CONTAINER IMMAGINE DC-LOGO -->
            <div class="cont-img">
                
           
                <!-- LISTE CON I VARI LINK -->
                <div class="d-flex">
                    <ul> <h3 class="mt-3">DC COMICS</h3>
                        <li v-for= "(link, index) in comics" :key="index">
                            <a href="">{{ link.label }}</a></li>
                    </ul>
                    <ul><h3 class="mt-3">DC</h3>
                        <li v-for= "(utility, index) in comics" :key="index">
                            <a href="">{{ utility.link_utili }}</a></li>
                    </ul>
                    <ul><h3 class="mt-3">SITES</h3>
                        <li v-for= "(site, index) in comics" :key="index">
                            <a href="">{{ site.site }}</a></li>
                    </ul>
                </div>
                <!-- LISTA SHOP SOTTOSTANTE -->
                <div class= "pb-5">
                    <ul>
                        <h3 >SHOP</h3>
                        <li v-for= "(shop, index) in comics" :key="index">
                            <a href="">{{ shop.shop }}</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
    <!-- SECONDA PARTE FOOTER -->
    <div class="bg-grigio">
        <div class="container dis-flex">
            <!-- BOTTONE ISCRIVITI ORA -->
            <div class="col-2 my-3">
                <button class="my-2">SIGN-UP NOW!</button>
            </div>
            <!-- LINK SOCIAL TRAMITE ICONE -->
            <div class=" col-10 d-flex justify-end">
                <ul  class="d-flex"> <h4>FOLLOW US</h4>
                    <li class= "mx-2" v-for= "(icons, index) in social" :key="index"><a href=""><img :src="icons.icon" alt="icon-social" ></a></li>
                </ul>
            </div>
        </div>
    </div>
</template>
<style lang ="scss" scoped>
@use "../styles/partials/variables" as *;
/* IMG DI SFONDO */
.img-sfondo{
    background-image: url("/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
}
/* LOGO CON POSITION ABSOLUTE */
.logo{
    width: 400px;
    position: absolute;
}

/* COLORE TESTO H3 E H4*/
h3{
    color: white;
}
h4{
    color: $primary_color
}

/* STILE LI */
li{
    list-style-type: none;
    margin-top: 0;
    margin-bottom: 0;
 
    /* STILE TAG A ALL'INTERNO DI LI */
    a{
        text-decoration: $decorazione-testo;
        color: grey
    }
    /* HOVER DEL TAG A ALL'INTERNO DI LI */
    a:hover{
        color:white
    }
}

/* SECONDA PARTE FOOTER */
.bg-grigio {
    background-color: $color-grey;
}

/* STILE BOTTONE */
button{
    padding: 15px;
    background-color: $color-grey;
    border-color: $primary_color;
    color: white
}

/* CONTAINER LOGO DC */
.cont-img{
    background-image: url("/dc-logo-bg.png");
    background-position: right;
    background-repeat: no-repeat;
}

/* ANNULLAMENTO MARGINI DATI IN DEFAULT DA BOOTSTRAP*/
ul{
    margin-top:0;
    margin-bottom: 0;
}

/* DISPLAY FLEX E ALLINEAMENTO CENTRALE */
.dis-flex{
    display: flex;
    align-items: center;
}

/* ALLINEAMENTO ICONE FOOTER A SINSTRA */
.justify-end{
    justify-content: end
}

/* STILE SFONDO BONUS */
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
        padding: 30px 0px
    }
    li{
        margin: 10px
    }
    img{
        width: 60px
    }
    img:hover{
        width: 65px;
        transition: 0.5s;
        
    }
}

</style>