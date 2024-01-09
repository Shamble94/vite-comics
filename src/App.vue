<script>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"
import Bonus from "./components/Bonus.vue"
export default {
    components: {
      AppHeader,
      AppMain,
      AppFooter,
      Bonus
    }
  }
</script>
<template lang="">
  <div>
    <AppHeader/>
    <AppMain/>
    <Bonus />
    <AppFooter/>
  </div>
</template>

<style lang ="scss">
  @use "./styles/generals.scss";
  @use "./styles/partials/variables"
</style>