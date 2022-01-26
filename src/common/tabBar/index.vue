<template>
  <div id="tabBar">
    <ul>
      <router-link v-for="item,index in tabBar" :key="index" :to="item.path" v-slot="{navigate,isExactActive}"  custom>
        <li :class="[isExactActive && 'router-link-exact-active']" @click="navigate">
            <i v-html="item.icon" class="iconfont"></i>
            <span>{{item.title}}</span>
        </li>
      </router-link>
    </ul>
  </div>
</template>

<script type="text/javascript">
export default {
  name: "app",
  data() {
    return {
      tabBar: [
        {
          title: "电影",
          path: "/movie",
          icon: "&#xe624;",
        },
        {
          title: "影院",
          path: "/cinema",
          icon: "&#xe61a;",
        },
        {
          title: "我的",
          path: "/mine",
          icon: "&#xe610;",
        },
      ],
    };
  },
  created() {},
  components: {},
};
</script>

<style scoped>
#tabBar{
    width: 100%;
    height: 1rem;
    position: fixed;
    background:#fff;
    left: 0;
    bottom: 0;
    border-top:1px solid  #ccc;
}
#tabBar ul{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content:space-around;
    align-items:center;
}
#tabBar ul li{
    width: 40%;
    height: 100%;
    display: flex;
    flex-direction:column;
    justify-content:center;
    color: #333;
    font-size: .3rem;
}
#tabBar ul .router-link-exact-active{
    color: #e54847;
}
#tabBar ul li i{
    text-align: center;
    font-size: .4rem;
}
#tabBar ul li span{
    display: block;
    text-align: center;
    padding-top: .06rem;
}
</style>

