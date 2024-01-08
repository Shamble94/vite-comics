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

            <div class= "pb-5">
                <ul><h3 >SHOP</h3>
                        <li v-for= "(shop, index) in comics" :key="index">
                            <a href="">{{ shop.shop }}</a></li>
                    </ul>

            </div>
        </div>
    </div>
    <div class="bg-grigio">
        <div class="container dis-flex">
            <div class="col-2 my-3">
                <button class="my-2">SIGN-UP NOW!</button>
            </div>
       
            <div class=" col-10 d-flex justify-end">
                <ul  class="d-flex"> <h4>FOLLOW US</h4>
                    <li class= "mx-2" v-for= "(icons, index) in social" :key="index"><img :src="icons.icon" alt="icon-social" ></li>
                </ul>
            </div>
        </div>
    </div>
</template>
<style lang ="scss" scoped>
@use "../styles/partials/variables" as *;
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
    a{
        text-decoration: none;
        color: grey
    }
    a:hover{
        color:white
    }
}
.bg-grigio {
    background-color: rgba(48,48,48,255);
}
button{
    padding: 15px;
    background-color: rgba(48,48,48,255);
    border-color: $primary_color;
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
h4{
    color: $primary_color
}
.justify-end{
    justify-content: end
}
</style>