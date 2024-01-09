<script>
export default{
    name: "AppHeader",
    data(){
      return{
        /* ARRAY DEL NAV  */
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
          <!-- LINK -->
          <a href="/">
            <img src="/dc-logo.png" alt="logo-dc" class="logo">
          </a>
        </div>
        <!-- NAV CENTRATO ALL'INTERNO DI UNA COLONNA -->
        <div class="align-centro col-7 ">
          <ul>
            <!-- CICLO V-FOR PER CREARE IL NAV PRENDENDO I DATI DALL'ARRAY NAV_LINK -->
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
    /* STILE UL, LI E A:HOVER */
    ul {
     
      display: flex;
      li{ 
        list-style-type: none;
        margin: 5px;
        font-weight: 700;
      }
      a:hover{
      color: $primary_color;
    }
    }
    /* ALLINEAMENTO CENTRALE */
    .align-centro{
      display:flex;
      align-items: center;
    }
    /* DIMENSIONI LOGO */
    .logo{
      width: 100px;
    
    }
    /* STILE ELEMENTO ACTIVE */
    .active{
      color: $primary_color;
      border-bottom: 3px solid $primary_color;
      
    }
    /* STILE TAG A */
    a{
      text-decoration: $decorazione-testo;
      color: black;
      /* position: relative;
 */
      /* &::after{
        content: "";
        position: absolute;
        bottom: 0;
        left: 10px;
        width: calc(100% - 20px);
        height: 3px;
        background-color: $primary_color
      } */
    }
   
</style>