<script>
export default{
    name: "AppHeader",
    data(){
      return{

      }
    }
}
</script>
<template lang="">
  <header>
    <div class="container m-3">
      <div class="row">
        <div class="col-5">
          <a href="/">
            <img src="/dc-logo.png" alt="logo-dc" class="logo">
          </a>
        </div>   
        <div class="d-flex col-7 ">
          <ul>
            <li>CHARACTERS</li>
            <li class="active">COMICS</li>
            <li>MOVIES</li>
            <li>TV</li>
            <li>GAMES</li>
            <li>COLLECTIBLES</li>
            <li>VIDEOS</li>
            <li>FANS</li>
            <li>NEWS</li>
            <li>SHOP</li>
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