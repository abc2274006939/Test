<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button" style="border: 1px solid #ccc">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper" v-for="item of hot" :key="item.id">
            <div class="button" style="border: 1px solid #ccc">{{item.name}}</div>
          </div>
        </div>
      </div>
      <div class="area" v-for="(item,key) of cities" :key="key" :ref="key">
        <div class="title border-topbottom">{{key}}</div>
        <div class="item-list">
          <div class="item border-bottom" style="border-bottom: .02rem solid #ccc" v-for="innerItem of item" :key="innerItem.id">{{innerItem.name}}</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  props:{
  hot:Array,
  cities:Object,
  letter:String
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  },
  watch:{
    letter(){
      if(this.letter){
        const element=this.$refs[this.letter][0]
        this.scroll.scrollToElement(element)
      }
    }

  }
}
</script>

<style lang="stylus" scoped>
.border-topbottom
  &:before
    border-bottom:#ccc
  &:after
    border-bottom:#ccc
.list
    overflow:hidden
    position:absolute
    top:4.60rem
    left:0
    right:0
    bottom:0
.title
    line-height:1.4rem
    background:#eee
    padding-left:.2rem
    color:#666
    font-size:.82rem
.button-list
     overflow:hidden
     padding:.10rem .6rem .1rem .1rem
.button-wrapper
     float:left
     width:33.33%
.button
     font-size:.80rem
     margin:.80rem
     text-align:center
     margin:.1rem
     padding:.1rem 0
     border-radius:.06rem
.item-list
 .item
    line-height:1.54rem
    padding-left:.2rem
</style>
