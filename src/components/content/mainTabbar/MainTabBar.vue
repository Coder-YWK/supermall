<template>
  <tab-bar>
    <tab-bar-item path='/home'>
      <!--在DOM中的属性，如src中使用路径别名时，需要在路径别名前加上一个"~"，而在import中使用则不需要，直接使用别名即可-->
      <img slot="item-icon" src="~assets/img/tabbar/home.svg">
      <img slot="item-icon-active" src="~assets/img/tabbar/home-active.svg">
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path='/category'>
      <img slot="item-icon" src="~assets/img/tabbar/category.svg">
      <img slot="item-icon-active" src="~assets/img/tabbar/category-active.svg">
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path='/cart'>
      <img slot="item-icon" src="~assets/img/tabbar/shopcart.svg">
      <img slot="item-icon-active" src="~assets/img/tabbar/shopcart-active.svg">
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path='/profile'>
      <img slot="item-icon" src="~assets/img/tabbar/profile.svg">
      <img slot="item-icon-active" src="~assets/img/tabbar/profile-active.svg">
      <div slot="item-text">我的</div>
    </tab-bar-item>
    </tab-bar>
</template>

<script>
import TabBar from 'components/tabbar/TabBar'
import TabBarItem from 'components/tabbar/TabBarItem'

export default {
  name:'MainTabBar',
  components: {
    TabBar,
    TabBarItem
  },
  props: {},
  data() {
    return {
    }
  },
  watch: {},
  computed: {},
  methods: {},
  created() {},
  mounted() {}
}
</script>

<style scoped>
</style>