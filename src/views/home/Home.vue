<template>
<div id="home">
  <nav-bar class="home-nav">
    <template v-slot:center>
      购物街
    </template>
  </nav-bar>
</div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'
import { getHomeMultidata } from 'network/home'

export default {
  name: 'Home',
  components: {
    NavBar
  },
  data () {
    return {
      banner: [],
      recommends: []
    }
  },
  created () {
    getHomeMultidata().then((res) => {
      console.log(res)
      this.banner = res.data.banner.list
      this.recommends = res.data.recommend.list
    })
  }
}
</script>

<style lang="scss" scoped>
.home-nav{
  background-color: var(--color-tint);
  color:#ffffff;
}
</style>
