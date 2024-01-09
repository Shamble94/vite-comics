<script>
export default{
    name: "CardComics",
    props: {
      comic: Object
    }
}
</script>

<template lang="">
  
    <div class ="comic_card mt-3"  :key="index">
      <img :src="comic.thumb" alt="">
      <h6>{{ comic.series }}</h6>
    </div>
</template>
<style lang ="scss" scoped>
@use "../styles/partials/variables" as *;

.comic_card{
  width: calc(100% / 6 - 20px);
  margin: 10px;

}

img{
  width: 100%;
  height: 60%
}
</style>