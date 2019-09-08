<template>
  <div>
    <!-- header -->
    <app-header :poiInfo="poiInfo"></app-header>
    <!-- navigation -->
    <app-nav :commentNum="commentNum"></app-nav>
    <!-- content -->
    <keep-alive>
      <router-view></router-view>
    </keep-alive>
  </div>
</template>

<script>
import Header from './components/header/Header'
import Nav from '@/components/nav/Nav'
import Goods from '@/components/goods/Goods';
import Ratings from '@/components/ratings/Ratings';
import Seller from '@/components/seller/Seller';
import VueRouter from 'vue-router';
import Vue from 'vue'
Vue.use(VueRouter)
const routes = [
  {path:'/',redirect:'/goods'},
  {path:"/goods",component:Goods},
  {path:"/ratings",component:Ratings},
  {path:"/seller",component:Seller}
]

// 实例化router
const router = new VueRouter({
  routes,
  linkActiveClass:"active"
})
export default {
  name: 'Home',
  router,
  data(){
    return{
      poiInfo:{},
      commentNum:0
    }
  },
  components: {
    "app-header":Header,
    "app-nav":Nav,
  },
  created(){
    fetch("/api/goods")
      .then(res => {
        return res.json()
      })
      .then(response =>{
        if(response.code == 0){
          this.poiInfo = response.data.poi_info
        }
      })

    // 请求ratings
    fetch("/api/ratings")
      .then(res => {
        return res.json()
      })
      .then(response =>{
        if(response.code == 0){
          this.commentNum = response.data.comment_num
        }
      })
  }
}
</script>

<style>

</style>
