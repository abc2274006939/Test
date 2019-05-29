<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul class="ulli">
      <router-link  tag="li" :to="'/detail/'+item.id" class="item border-bottom" v-for="item  of  list" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>
<script>
export default {
    name: 'HomeRecommend',
    props:{
      list:Array
    },
}
</script>
<style lang="stylus" scoped>
.recommend-title {
  margin-top: 0.2rem
  line-height: 2rem
  background: #eee
  text-indent: 0.2rem
}

.item {
  overflow: hidden
  display: flex
  height: 5.9rem
}

.ulli {
  padding: 0px
}

.item-img {
  width: 6.7rem
  height: 5.7rem
  padding: 0.1rem
  padding-right: 0.2rem
}

.item-info {
  flex: 1
  padding: 0.1rem
}

.item-title {
  margin: 0
  line-height: 1.2rem
  line-height: 1.54rem
  font-size: 0.88rem
}

.item-desc {
  margin: 0
  line-height: 1.4rem
  color: #ccc
}

.item-button {
  margin-top: 0.16rem
  background: #ff9300
  padding: 0 0.44rem
  border-radius: 0.2rem
  border: none
  color: #fff
  line-height: 1.44rem
}
</style>
