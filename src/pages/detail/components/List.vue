<template>
<div>
  <div class="item" v-for="(item,index) of list"  :key="index"  >
      <div class="item-title  border-bottom">
          <span class="item-title-icon">
              {{item.title}}
          </span>
      </div>
      <div class="show" >
      <div class="item-one" >
          <h3 class="item-h3">[周末促销]故宫门票</h3>
          <div class="item-two">
              ¥
              <span>45.9</span>
              <span>起</span>
              <transition name="slide-fade">
                <div class="item-serve iconfont" @click="one_h(index)">&#xe612;</div>
              </transition>
          </div>
      </div>
      <div class="yingchang" v-show="index== Oindex">
      <div class="left_one">
          <div class="yinc">
              <div class="left">
                  <h6 class="yic_h6">故宫博物馆学生票(周末特惠20.9元)</h6>
                  <ul class="ul_one">
                      <span class="ul_sre">
                          <img src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" class="img_o"/>
                          可订明日
                      </span>
                  </ul>
                  <ul class="ul_ones">
                      <span class="spass">
                         无需换票
                      </span>
                      <span class="spass">
                          不可退
                      </span>
                  </ul>
                <div class="spass_one">
                  <span>去哪儿直销</span>
                  <span>预订须知</span>
                  <span></span>
                 </div>
             </div>
          <div class="right">
             <a href="JavaScript:;" class="a_one">
                 <strong class="style_one">
                     ¥
                     <span>20.9</span>
                 </strong>
                 <div class="em_one">预订</div>
             </a>
          </div>
      </div>
          </div>
           <div class="yingchang">
          <div class="yinc">
              <div class="left">
                  <h6 class="yic_h6">故宫博物馆成人票(周末特惠45.9元)</h6>
                  <ul class="ul_one">
                      <span class="ul_sre">
                          <img src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" class="img_o"/>
                          可订明日
                      </span>
                  </ul>
                  <ul class="ul_ones">
                      <span class="spass">
                         无需换票
                      </span>
                      <span class="spass">
                          不可退
                      </span>
                  </ul>
                <div class="spass_one">
                  <span>去哪儿直销</span>
                  <span>预订须知</span>
                  <span></span>
                 </div>
             </div>
          <div class="right">
             <a href="JavaScript:;" class="a_one">
                 <strong class="style_one">
                     ¥
                     <span>45.9</span>
                 </strong>
                 <div class="em_one">预订</div>
             </a>
          </div>
      </div>
  </div>
   <div class="yingchang">
          <div class="yinc">
              <div class="left">
                  <h6 class="yic_h6">故宫博物馆儿童票(周末特惠20.9元)</h6>
                  <ul class="ul_one">
                      <span class="ul_sre">
                          <img src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png" class="img_o"/>
                          可订明日
                      </span>
                  </ul>
                  <ul class="ul_ones">
                      <span class="spass">
                         无需换票
                      </span>
                      <span class="spass">
                          不可退
                      </span>
                  </ul>
                <div class="spass_one">
                  <span>去哪儿直销</span>
                  <span>预订须知</span>
                  <span></span>
                 </div>
             </div>
          <div class="right">
             <a href="JavaScript:;" class="a_one">
                 <strong class="style_one">
                     ¥
                     <span>20.9</span>
                 </strong>
                 <div class="em_one">预订</div>
             </a>
          </div>
          
      </div>
       </div>
  </div>
      <div v-if="item.children" class="item-chilren"> 
      </div>
  </div>
  </div>
</div>
</template>
<script>
export default {
    name:'DetailList',
    data() {
        return {
            k_one:false,
            Oindex: 0
        }
    },
    props:{
        list:Array
    },
    mounted() {
        console.log(this.list[0].title)
    },
     methods: {
         one_h(index){
           this.Oindex  = index
         },
     }
}
</script>
<style lang="stylus" scoped>
.item-title-icon
    position :relative
    left :.06rem
    top:.08rem
    display :inline-block
    width :80%
    height :2.36rem
    font-size :0.80rem
    background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0  0.68rem no-repeat
    background-size :1.4rem 11rem
    padding-left :1.2rem
    width :100%
    border-bottom 1px  solid #dadada
.item-title
   line-height 2.8rem
   padding 0  .2rem
.item-chilren
   padding :0 .6rem
   font-size :0.9rem
.item-h3
    margin: 0 1.8rem 0 0
    color: #333;
    font-size: 0.80rem;
    line-height: 1.48rem
    padding-left: 7px
    font-weight :normal
.item-two
    top: 35px;
    float: right;
    margin-top: -1.28rem;
    margin-right: 12px;
    color: #ff9800;
.item-serve
    float: right;
    color: #bbb;
    font-size: 0.90rem
.item-one
    padding: .24rem .2rem
.yinc 
    background: #f5f5f5
    box-sizing: border-box;
    padding: .2rem
    overflow: hidden;
.yic_h6
    padding: 0;
    color: #616161;
    font-size: 0.80rem;
    font-weight :normal
    line-height: 1.4rem
    margin :0
.ul_sre
    display: inline-block;
    height: 0.80rem;
    color: #616161;
    font-size: .80rem;
    line-height: .32rem;
    white-space: nowrap
.img_o
    display: inline-block;
    width: 0.8rem;
    max-height: 0.80rem;
    margin-right: .04rem;
    vertical-align: 0;
.ul_one
     padding :0
     margin :0
.ul_ones
    padding :0
    margin :0
    margin-top :-5px
.spass
    display: inline-block;
    margin-top: 0.08rem;
    padding: 0 0.04rem;
    height: 0.80rem;
    color: #00afc7;
    font-size: 0.2rem;
    line-height: 0.80rem;
    white-space: nowrap;
    border-radius: .08rem;
    border: 1px solid #e0e0e0;
.spass_one 
    margin-top: .08rem;
    color: #616161;
    font-size: 0.80rem;
    line-height: 1.34rem
.a_one
    box-sizing: border-box;
    display: block;
    padding-right: 16px;
    text-decoration: none;
    width: 100%;
.style_one
    color: #ff9800;
    text-align: center;
    padding-right: 12px;
.left
  float :left
.em_one
    background: #ff9800;
    color: #fff;
    border-radius: 7px;
    height: 22px;
    text-align: center;
.right
   float :right
.yingchang
   border-bottom: 1px solid #dadada;
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}

</style>
