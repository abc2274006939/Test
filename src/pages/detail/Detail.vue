<template>
    <div>
        <detail-banner :sightName="sightName"
                       :bannerImg="bannerImg" 
                       :gallaryImgs="gallaryImgs">
        </detail-banner>
        <detail-header ></detail-header>
        <detail-ban></detail-ban>
        <detail-eve></detail-eve>
        <div class="content">
            <detail-list :list="list"></detail-list>
        </div>
          <detail-Ico></detail-Ico>
    </div>
</template>
<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import DetailBan from './components/Ban'
import DetailEve from './components/Eve'
import DetailIco from './components/Ico'
import axios from 'axios'
export default {
    name:'Detail',
    components:{
        DetailBanner,
        DetailHeader,
        DetailList,
        DetailBan,
        DetailEve,
        DetailIco
    },
   data(){
       return{
            sightName:" ",
            bannerImg:"",
            gallaryImgs:[],
            list:[{
               title:'成人票',
           },{
              title:'学生票',
              
           },{
               title:'儿童票'
           },{
               title:'特惠票'
           }],
       }

   },
  methods: {
       getDetailInfo(){
         axios.get('/api/detail.json',{
             params:{
               id:this.$route.params.id
             }
         }).then(this.handleGetDataSucc)
       },
       handleGetDataSucc(res){
          res=res.data
          if(res.ret&&res.data){
             const data=res.data
             this.sightName = data.sightName
             this.bannerImg = data.bannerImg
             this.gallaryImgs=data.gallaryImgs
          }
       }
     },
     mounted() {
         this.getDetailInfo()
  }
}
</script>
<style lang="stylus" scoped>

</style>
