<template>
<<<<<<< HEAD
  <el-carousel :interval="interval" :indicator-position="indicator" :arrow="arrow" height="100%" :autoplay="autoplay">
    <el-carousel-item v-for="item in data" :key="item.id">
      <a :href="item.url || 'javascript:;'"><img :src="item.pic"></a>
=======
  <el-carousel :interval="interval" :indicator-position="indicator"     :arrow="arrow" height="100%" :autoplay="autoplay">
    <el-carousel-item v-for="item in data" :key="item.id">
      <router-link :to="item.url"><img :src="item.pic"></router-link>
>>>>>>> remotes/origin/master
    </el-carousel-item>
  </el-carousel>
</template>
<script>
export default {
  name: 'absBox',
  data () {
    return {}
  },
  props: {
    data: {
      type: [Array]
    },
    interval: {
      type: [Number, String],
      default: 4000
    },
    indicator: {
      type: [String],
      default: ''
    },
    arrow: {
      type: [String],
      default: 'hover'
    },
    autoplay: {
      type: [Boolean],
      default: true
    }
  }
}

</script>
<style scoped>
</style>
