<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont ">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont" style="font-size: .30rem;">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props:{
    city:String
  }
}
</script>
<style lang="stylus" scoped>
.header {
  display: flex;
  line-height: 1.86rem;
  background: #00bcd4;
  color: #fff;
}

.header-left {
  width: 2.64rem;
  float: left;
  text-align: center;
  line-height: 36px;
}

.header-input {
  flex: 1;
  height: 1.5rem;
  margin-top: 0.39rem;
  margin-left: 0.2rem;
  padding-left: 0.2rem;
  background: #fff;
  border-radius: 0.1rem;
  color: #CCC;
  font-size: 13px;
  line-height: 24px;
}

.header-right {
  width: 3.9rem;
  float: right;
  text-align: center;
  line-height: 2.36rem;
  color: #fff;
}
</style>