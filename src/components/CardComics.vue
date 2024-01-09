<script>
export default{
    name: "CardComics",
    props: {
      comic: Object
    }
}
</script>

<template lang="">
  <div class="comics-container">
    <div class ="comic_card mt-3"  :key="index">
      <img :src="comic.thumb" alt="">
      <h6>{{ comic.series }}</h6>
    </div>

  </div>
</template>
<style lang ="scss" scoped>
@use "../styles/partials/variables" as *;

.comic_card{
  width: calc(100% / 6 - 20px);
  margin: 10px;

}
.comics-container{
 display: flex;
 flex-wrap: wrap;
}
</style>