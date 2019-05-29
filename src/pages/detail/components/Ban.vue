<template>
<div>
    <div class="Ban_one">
        <div class="Ban_two">
       <div class="ban_one">
         <div>
           <span class="span_one">5.0</span>
           <span class="span_two">分</span>
           <span class="span_serve">超赞</span>
         </div>
         <div>
         <span class="ban_one">359425条评论</span>
         <span class="ban_two">93条攻略</span>
         <span class="ban_serve iconfont">&#xe62f;</span>
         </div>
       </div>
       <div class="ban_tw">
          <div>
          <span class='list_one'>景点简介</span>
          </div>
          <div>
           <span class="list_two">开放时间、贴士</span>
           <span class="ban_server iconfont">&#xe62f;</span>
          </div>
       </div>
    </div>
     <div class="P_one">
          <p class="p_two">
            <span class="iconfont ic_one">&#xe610;</span>
            <span class="p_span">北京市东城区景山前街4号</span>
            <span class="span_pe iconfont">&#xe62f;</span>
          </p>
       </div>
    </div>
</div>
</template>
<script>
export default {
    name:'DetaliBan'
}
</script>
<style lang="stylus" scoped>
.Ban_one
    position: relative;
    top: -.1rem;
    padding: .1rem .2rem 0 .2rem;
    margin-bottom: .1rem;
    background: #fff;
    -webkit-border-radius: .1rem .1rem 0 0;
    -moz-border-radius: .1rem .1rem 0 0;
    border-radius: .1rem .1rem 0 0;
.Ban_two
    padding-top: .6rem
    height: 38px
    padding-bottom: .5rem
    border-bottom: 1px solid #dadada;
.ic_one
    line-height: 20px
    position: absolute
    left: 16px
.span_one
    font-size: 1.4rem
    color: #ff8300
    line-height: .60rem
    float: left
.span_two
    font-size: 0.80rem
    color: #ff8300
    line-height: .58rem
.span_serve
    font-size: 0.80rem
    color: #ff8300
    line-height: .58rem
    margin-left: .2rem
.ban_one
    font-size: 0.70rem
    color: #9e9e9e
    line-height: 1.2rem
    margin-right: .2re
    float:left
.ban_two
    font-size: 0.70rem
    color: #9e9e9e
    line-height: 1.2rem
    margin-left :.2rem
.ban_serve
    position: absolute;
    top: 0.8rem;
    right: 12.2rem;
    color: #9e9e9e;
    font-size: 0.8rem;
.ban_tw
    font-family: Arial,"Microsoft Yahei","Helvetica Neue",Helvetica,sans-serif
    color: #212121
    float:right
    font-size: .28rem
    line-height: 11px;
    margin-right: 2pc;
    border-left :1px solid #dadada
.list_one
    font-size: .85rem
    color: #212121
    line-height: .48rem
    padding: 0  1.6rem
.list_two
    color: #9e9e9e;
    font-size: .70rem;
    padding: 0  1.6rem
    line-height: 22px
.ban_server
    position: absolute;
    top: 0.90rem;
    left: 331px;
    color: #9e9e9e;
    font-size: 0.80rem
.P_one
    display: block
    height: 24px
    position: relative
    padding: .2rem 0
    line-height: .36rem
    background :#f5f5f5

.p_two
    position: relative
    margin :0
.p_span
    line-height: 20px
    position: absolute
    left: 47px
    top: 0.16rem;
    font-size: 14px
.span_pe
    position: absolute
    right: 11px
    top: -5px
    margin-top: 0.80rem
    color: #9e9e9e
    font-size: 0.90rem
</style>
