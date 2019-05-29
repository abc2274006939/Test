<template>
<div>
   <router-link tag="div" to="/" class="header-abs"  v-show="showAbs">
       <div class="iconfont header-abs-back">&#xe624;</div>
   </router-link >
    <div class="header-fixed"  v-show="!showAbs" :style="opacityStyle">
           <router-link to="/">
      <div class="iconfont header-fixed-back">&#xe624;</div>
       </router-link>
        景点详情
    </div>
</div>
</template>
<script>

export default {
    name:'DetailHeader',
    data(){
        return{
             showAbs:true,
             opacityStyle:{
                 opacity:0
             }
        }
    },
    methods: {
       handleScroll () {
           const top=document.documentElement.scrollTop
           if(top>60&&top<150){
               const opacity=top/150
               this.opacityStyle={opacity}
               this.showAbs=false
           }else{
               this.showAbs=true
           }
       }
    },
    mounted() {
        window.addEventListener('scroll',this.handleScroll)
    }
}
</script>
<style lang="stylus" scoped>
.header-abs
   position :absolute
   top :.8rem
   left :.8rem
   width :2rem
   height :2rem
   line-height :.8rem
   border-radius :1rem
   background :rgba(0,0,0,.8)
.header-abs-back
   color :#fff
   font-size :1rem
   line-height: 32px;
   text-align: center;
.header-fixed
    z-index:2 
    position:fixed
    top :0
    right: 17px;
    left: -1px;
    height:2rem
    line-height:1.86rem
    text-align:center
    color:#fff
    background:#00bcd4
    font-size:.90rem
.header-fixed-back
    position:absolute
    top:2px
    left:12px
    width:.64rem
    text-align:center
    font-size:1rem
    color:#fff
</style>
