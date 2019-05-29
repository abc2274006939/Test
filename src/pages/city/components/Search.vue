<template>
  <div>
    <div class="sercha">
      <input v-model="k_one" class="search-input" type="text" placeholder="输入城市名或拼音">
    </div>
    <div class="search-content" ref="search" v-show="k_one">
      <ul class="a_one">
        <li class="search-item  border-bottom" v-for="item of list" :key="item.id">{{item.name}}</li>
        <li class="search-item  border-bottom" v-show="!list.length">没有找到匹配数据</li>
      </ul>
    </div>
  </div>
</template>
<script>
import ball from 'better-scroll'
export default {
  name: "CitySearch",
  props: {
    cities: Object
  },
  data() {
    return {
      k_one:'',
      list: [],
      time: null
    };
  },
  watch: {
    k_one() {
      if (this.time) {
        clearTimeout(this.time)
      }
      if(!this.k_one){
        this.list=[]
        return
      }
      this.time = setTimeout(() => {
        const result=[]
        for(let i in this.cities){
          this.cities[i].forEach((value)=>{
            if(value.spell.indexOf(this.k_one)>-1||value.name.indexOf(this.k_one)>-1){
              result.push(value)
            }
          })
        }
        this.list=result
      }, 100)
    }
  },
  mounted() {
    this.scroll=new  ball(this.$refs.search)
    
  },
}
</script>

<style lang="stylus" scoped>
.sercha {
  height: 2.1rem;
  padding: 0 0.2rem;
  background: #00bcd4;
}
.search-input {
  box-sizing: border-box;
  width: 100%;
  height: 1.6rem;
  padding: 0 0.1rem;
  line-height: 0.62rem;
  text-align: center;
  border-radius: 0.6rem;
  border: none;
  color: #666;
}
.a_one
  margin-top :0
.search-content {
  z-index :1
  overflow: hidden;
  background:#eee;
  position: absolute;
  top: 3.90rem;
  left: -40px;
  right: 0;
  bottom: 0;
}
.search-item
  line-height :1.62rem
  padding-left :.2rem
  background :#fff
  color :#666
</style>
