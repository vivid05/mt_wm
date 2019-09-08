<template>
  <div id="container">
      <van-nav-bar
        title="城市选择"
        left-text="返回"
        @click-left="onClickLeft"
        fixed
        z-index=5
        />
      <van-index-bar >
          <div v-for="(item,index) of cities" :key="index" >
            <van-index-anchor sticky :index="index" />
            <van-cell @click="changeCity(innerItem.name)" v-for="innerItem of item" :key="innerItem.id"  :title="innerItem.name" />
          </div>     
</van-index-bar>
  </div>
</template>
<script>
import Vue from 'vue'
import { IndexBar, IndexAnchor,Cell, CellGroup,NavBar  } from 'vant';
Vue.use(IndexBar).use(IndexAnchor).use(Cell).use(CellGroup).use(NavBar);
import axios from 'axios'
export default {
    data(){
        return {
            cities:{}
        }
    },
    methods:{
        onClickLeft(){
            this.$router.push('/')
        },
        getCity(){
            axios.get('./../../../static/city.json')
            .then(res=>{
                this.cities=res.data.data.cities
                // for(var item in res.data.data.cities){
                //     this.cities.push(item)
                // }
            })
            .catch(err=>{
                console.log(err)
            })
        },
        changeCity(city){
            this.$emit('changeCity',city)
            this.$router.push('/')
        }
    },
    created(){
        this.getCity()
    }
}
</script>

<style>
.van-index-anchor--sticky{
    top:46px;
}
.van-index-bar{
    margin-top: 46px;
}
</style>