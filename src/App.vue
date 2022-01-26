<template>
   <div id="app">
       <TabBar></TabBar>
       <keep-alive>
           <router-view></router-view>
       </keep-alive>
   </div>
</template>

<script type="text/javascript">
import TabBar from "./common/tabBar/index.vue"
export default {
   name: "app",
   data() {
       return {

       }
   },
   created(){

   },
   components: {
       TabBar
   }
}
</script>

<style lang="scss" scoped>
</style>
