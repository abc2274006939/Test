<template>
  <div class="header">城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>

.header
    position:relative
    overflow:hidden
    height:2rem
    line-height:1.86rem
    text-align:center
    color:#fff
    background:#00bcd4
    font-size:.90rem
.header-back
    position:absolute
    top:2px
    left:12px
    width:.64rem
    text-align:center
    font-size:1rem
    color:#fff
</style>
