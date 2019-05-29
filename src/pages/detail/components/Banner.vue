<template>
<div>
    <div class="banner" @click="hann">
        <img  class="banner-img" :src="bannerImg"/>
        <div class="banner-info">
            <div class="banner-title">{{this.sightName}}</div>
             <div class="banner-number"><span class="iconfont banner-icon">&#xe692;</span>
             {{this.gallaryImgs.length}}
             </div>
        </div>
    </div>
    <common-gallary :imgs="gallaryImgs" v-show="showGallary"  @close="hand"></common-gallary>
</div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
    name:'DetailBanner',
    props:{
        sightName:String,
        bannerImg:String,
        gallaryImgs:Array
    },
    data(){
        return{
        showGallary :false,
       }
    },
    methods: {
        hann(){
            this.showGallary=true
        },
        hand(){
            this.showGallary=false
        }
    },
    components:{
        CommonGallary
    },
    mounted() {
        console.log(this.bannerImg)
    },
}
</script>
<style lang="stylus" scoped>
.banner
   position :relative
   overflow :hidden
   height :0
   padding-bottom :55%
.banner-img
   width :100%
.banner-info
   display :flex
   position :absolute
   left :0
   right :0
   bottom :0
   line-height :.6rem
   color :#fff
   background-image :linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
.banner-title
   flex :1
   padding :0 .32rem
.banner-number
    margin-top :.14rem
    padding :0 .6rem
    line-height :1rem
    height :1.2rem
    border-radius :0.2rem
    background :rgba(0,0,0,.8)
    font-size :.24rem
.banner-icon
    font-size :.24rem
    margin-right :2px;

</style>
