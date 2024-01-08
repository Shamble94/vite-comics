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
        <div class="align-centro col-7 ">
          <ul>
            <li v-for= "(links, index) in nav_link" :key="index">
              <a href="/" :class="links.active ? `active` : `` ">{{ links.link }}</a></li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>
<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
    ul {
     
      display: flex;
      li{ 
        list-style-type: none;
        margin: 5px;
        font-weight: 700;
      }
      a:hover{
      color: $primary_color;
      border-bottom: 3px solid $primary_color
    }
    }
    .align-centro{
      display:flex;
      align-items: center;
    }
    .logo{
      width: 100px;
    }
    .active{
      color: $primary_color;
      border-bottom:3px solid $primary_color;
    }
    a{
      text-decoration: none;
      color: black
    }
   
</style>