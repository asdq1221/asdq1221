<template>
  <div id="app">
<router-view></router-view>
    <FooterGuide v-show="$route.meta.showFooter"></FooterGuide>
  
</div>
</template>

<script>
import FooterGuide from './components/FooterGuide/FooterGuide.vue'
import {reqFoodTypes} from './api'
    export default {
     async mounted(){
       console.log("试试")
       const result = await reqFoodTypes()
       console.log(result)
      },
     components: {FooterGuide}
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
// #app {
//   font-family: 'Avenir', Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   text-align: center;
//   color: #2c3e50;
//   margin-top: 60px;
// }
#app
  width 100%
  height 100%
  background #f5f5f5
</style>
