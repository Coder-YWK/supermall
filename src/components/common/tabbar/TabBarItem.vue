<template>
  <div id="tab-bar-item" class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive"><slot name='item-icon'></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <div :style="activeStyle"><slot name='item-text'></slot></div>
  </div>
</template>

<script>
export default {
  name:'TarBarItem',
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'red'
    }
  },
  data() {
    return {
    }
  },
  computed: {
    isActive() {
      return this.$route.path.indexOf(this.path) !==-1 //indeOf函数在前者中找不到后者便返回-1
    },
    activeStyle() {
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  components: {

  },
  methods: {
    itemClick() {
      if(this.$router.history.current.path !== this.path) {//this.$router.history.current.path指当前路径
        this.$router.push(this.path)
      }
    }
  },
}
</script>

<style scoped>

  .tab-bar-item {
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 12px;

  }

  .tab-bar-item img {
    width: 24px;
    height: 24px;
    margin-top: 3px;
    vertical-align: middle;
    margin-bottom: 2px;
  }

</style>