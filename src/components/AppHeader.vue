<script>
export default{
    name: "AppHeader",
    data(){
      return{
        nav_link:[
            {
                link: "CHARACTERS",
                active: false
            },
            {
                link: "COMICS",
                active: true
            },
            {
                link: "MOVIES",
                active: false
            },
            {
                link: "TV",
                active: false
            },
            {
                link: "GAMES",
                active: false
            },
            {
                link: "COLLECTIBLES",
                active: false
            },
            {
                link: "VIDEOS",
                active: false
            },
            {
                link: "FANS",
                active: false
            },
            {
                link: "NEWS",
                active: false
            },
            {
                link: "SHOP",
                active: false
            }
        ]

      }
    }
}
</script>
<template lang="">
  <header>
    <div class="container my-3">
      <div class="row">
        <div class="col-5">
          <a href="/">
            <img src="/dc-logo.png" alt="logo-dc" class="logo">
          </a>
        </div>   
        <div class="d-flex col-7 ">
          <ul>
            <li v-for= "(shop, index) in nav_link" :key="index">{{ shop.link }}</li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>
<style lang="scss" scoped>
    ul {
      list-style-type: none;
      display: flex;
      li{
        flex-direction: row;
        margin: 5px;
        font-weight: 1000;
        font-size: 15px
      }
    }
    .d-flex{
      display:flex;
      align-items: center;
    }
    .logo{
      width: 100px;
    }
    .active{
      color: blue;
      border-bottom:3px solid blue;
    }
</style>