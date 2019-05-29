<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul class="ulli">
      <li class="item border-bottom" v-for="item  of  list" :key="item.id">
        <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
    name:'HomeWeekend',
    props:{
      list:Array
    }
}
</script>
<style lang="stylus" scoped>
.recommend-title {
  margin-top: 0.2rem
  line-height: 2rem
  background: #eee
  text-indent: 0.2rem
}
.item-img-wrapper{
    overflow :hidden
    height :0
    padding-bottom :37.09%

}
.ulli {
  padding: 0px
}

.item-img {
  width :100%
}
.item-title {
  margin: 0
  line-height: 1.2rem
  line-height: 1.54rem
  font-size: 0.88rem
}
.item-info{
    padding :.1rem
}

.item-desc {
  margin: 0
  line-height: 1.4rem
  font-size :11px
}
</style>