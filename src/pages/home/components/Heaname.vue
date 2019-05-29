<template>
    <div class="one_name">
        <ul class="ul_one">
            <li class="li_name li-tow">
                <span class="iconfont ">&#xe610;</span>
                定位失败
            </li>
            <li class="li_name">
                 <span class="iconfont ">&#xe60f;</span>
                必游榜单
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    name:"HomerHeaname"
}
</script>
<style lang="stylus" scoped>
.one_name
   width :100%
   background :#fff
   margin-top :10px
   border-top: 1px solid #e0e0e0;
.ul_one
   display :flex
   list-style :none
   display: inline-block;
   margin :0
   padding :0
   text-align: center
   line-height: 45px
.li_name
   display :inline
   justify-content :space-between
   float left
   width :172px
.li-tow
   border-right :1px solid #e0e0e0;
   display :block
   width: 179px;
</style>
