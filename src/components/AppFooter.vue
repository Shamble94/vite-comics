<script>
export default{
    name: "AppFooter",
    data(){
      return{
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
        ]

        }
      }
    }

</script>
<template lang="">
    <div class="sfondo ">
        <div class="container">
            <div class="cont-img">
                <img src="/dc-logo-bg.png" alt="dc-logo" class="logo">

            </div>
            <div class="d-flex">
                <ul> <h3 class="mt-3">DC COMICS</h3>
                    <li v-for= "(link, index) in comics" :key="index">{{ link.label }}</li>
                </ul>
                <ul><h3 class="mt-3">DC</h3>
                    <li v-for= "(utility, index) in comics" :key="index">{{ utility.link_utili }}</li>
                </ul>
                <ul><h3 class="mt-3">SITES</h3>
                    <li v-for= "(site, index) in comics" :key="index">{{ site.site }}</li>
                </ul>
            </div>
            <div class= "my-3">
                <ul><h3 >SHOP</h3>
                        <li v-for= "(shop, index) in comics" :key="index">{{ shop.shop }}</li>
                    </ul>

            </div>
    
        </div>
    </div>
    <div class="bg-grigio">
        <div class="container dis-flex">
            <div class="col-1">
                <button>SIGN UP</button>
            </div>
       
            <div class=" col-11 justify-end">
                <ul  class="d-flex"> FOLLOW US
                    <li class= "mx-2" v-for= "(icons, index) in social" :key="index"><img :src="icons.icon" alt=""></li>
                </ul>
            </div>
        </div>
    </div>
</template>
<style lang ="scss" scoped>
.sfondo{
    background-image: url("/footer-bg.jpg");
    position: relative;
}
.logo{
    width: 400px;
    position: absolute;

}
h3{
    color: white;
   
}
li{
    color: grey;
    list-style-type: none;
    margin-top: 0;
    margin-bottom: 0;
}
.bg-grigio {
    background-color: grey;
}
button{
    margin: 10px;
    padding: 10px;
    background-color: grey;
    border-color: blue;
    color: white
}
.cont-img{
    display: flex;
    justify-content: end;
}
ul{
    margin-top:0;
    margin-bottom: 0;
}
.dis-flex{
    display: flex;
    align-items: center;
}

</style>