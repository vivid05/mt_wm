<template>
  <div>
      <div class="header">
        <transition>
          <div v-if="flag" class="address">
          <img src="../../assets/images/icon-地点.png" alt="">
          <router-link to="/city" tag="p"><p>{{currentCity}}</p></router-link>
        </div>
        </transition>      
        <div class="search">
          <img src="../../assets/images/搜索.png" alt="">
          <input disabled readonly type="text" placeholder="请输入商家或商品名称">
        </div>
        
      </div>
      <div  ref="foodList">
        <div class="icons">
        <div class="icons-item">
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/1.png" alt="">
              </div>
              <div class="icons-dec">美食</div>
            </div>
          </a>
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/2.png" alt="">
              </div>
              <div class="icons-dec">美团超市</div>
            </div>
          </a>
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/3.png" alt="">
              </div>
              <div class="icons-dec">生鲜果蔬</div>
            </div>
          </a>
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/4.png" alt="">
              </div>
              <div class="icons-dec">美团专送</div>
            </div>
          </a>
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/5.png" alt="">
              </div>
              <div class="icons-dec">快食简餐</div>
            </div>
          </a>
        </div>
        <div class="icons-item">
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/1.png" alt="">
              </div>
              <div class="icons-dec">美食</div>
            </div>
          </a>
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/2.png" alt="">
              </div>
              <div class="icons-dec">美团超市</div>
            </div>
          </a>
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/3.png" alt="">
              </div>
              <div class="icons-dec">生鲜果蔬</div>
            </div>
          </a>
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/4.png" alt="">
              </div>
              <div class="icons-dec">美团专送</div>
            </div>
          </a>
          <a class="icons-wrapper" href="#">
            <div>
              <div class="icons-img">
                <img src="../../assets/images/5.png" alt="">
              </div>
              <div class="icons-dec">快食简餐</div>
            </div>
          </a>
        </div>
      </div>
      <div class="seller">
        ——附近商家——
      </div>
      <div :class="[{classify:isActive},{_classify:!isActive}]">
        <ul>
          <li class="active">综合排序</li>
          <li>销量最高</li>
          <li>距离最近</li>
          <li>筛选</li>
        </ul>
      </div>
      <div>
        <ul>
          <li>
            <router-link to="buy" tag="div">
              <div class="restayrant">
              <div class="res-img">
                <img src="../../assets/images/6.jpg" alt="">
              </div>
              <div class="res-dec">
                <h3>肯德基(城东广场店)</h3>
                <div class="start">
                  <div class="left"><start :score='4.7'></start><span class="score">4.7</span><span class="num">月售6666</span></div>
                  <div class="right">30分钟|1.7km</div>
                </div>
                <div class="send">起送¥10|配送¥4|人均¥19</div>
                <div class="sell">
                  <p>
                    <img src="../../assets/images/满减.png" alt="">
                    <span>满25减11|满40减18|满60减22</span>
                  </p>
                  <p>
                    <img src="../../assets/images/折扣.png" alt="">
                    <span>折扣商品5折起</span>
                  </p>
                </div>
              </div>
            </div>
            </router-link>          
          </li>
          <li>
            <div class="restayrant">
              <div class="res-img">
                <img src="../../assets/images/9.jpg" alt="">
              </div>
              <div class="res-dec">
                <h3>肯德基(城东广场店)</h3>
                <div class="start">
                  <div class="left"><start :score='4.7'></start><span class="score">4.7</span><span class="num">月售6666</span></div>
                  <div class="right">30分钟|1.7km</div>
                </div>
                <div class="send">起送¥10|配送¥4|人均¥19</div>
                <div class="sell">
                  <p>
                    <img src="../../assets/images/满减.png" alt="">
                    <span>满25减11|满40减18|满60减22</span>
                  </p>
                  <p>
                    <img src="../../assets/images/折扣.png" alt="">
                    <span>折扣商品5折起</span>
                  </p>
                </div>
              </div>
            </div>
          </li>
          <li>
            <div class="restayrant">
              <div class="res-img">
                <img src="../../assets/images/7.jpg" alt="">
              </div>
              <div class="res-dec">
                <h3>肯德基(城东广场店)</h3>
                <div class="start">
                  <div class="left"><start :score='4.7'></start><span class="score">4.7</span><span class="num">月售6666</span></div>
                  <div class="right">30分钟|1.7km</div>
                </div>
                <div class="send">起送¥10|配送¥4|人均¥19</div>
                <div class="sell">
                  <p>
                    <img src="../../assets/images/满减.png" alt="">
                    <span>满25减11|满40减18|满60减22</span>
                  </p>
                  <p>
                    <img src="../../assets/images/折扣.png" alt="">
                    <span>折扣商品5折起</span>
                  </p>
                </div>
              </div>
            </div>
          </li>
          <li>
            <div class="restayrant">
              <div class="res-img">
                <img src="../../assets/images/8.jpg" alt="">
              </div>
              <div class="res-dec">
                <h3>肯德基(城东广场店)</h3>
                <div class="start">
                  <div class="left"><start :score='4.7'></start><span class="score">4.7</span><span class="num">月售6666</span></div>
                  <div class="right">30分钟|1.7km</div>
                </div>
                <div class="send">起送¥10|配送¥4|人均¥19</div>
                <div class="sell">
                  <p>
                    <img src="../../assets/images/满减.png" alt="">
                    <span>满25减11|满40减18|满60减22</span>
                  </p>
                  <p>
                    <img src="../../assets/images/折扣.png" alt="">
                    <span>折扣商品5折起</span>
                  </p>
                </div>
              </div>
            </div>
          </li>
          <li>
            <div class="restayrant">
              <div class="res-img">
                <img src="../../assets/images/6.jpg" alt="">
              </div>
              <div class="res-dec">
                <h3>肯德基(城东广场店)</h3>
                <div class="start">
                  <div class="left"><start :score='4.7'></start><span class="score">4.7</span><span class="num">月售6666</span></div>
                  <div class="right">30分钟|1.7km</div>
                </div>
                <div class="send">起送¥10|配送¥4|人均¥19</div>
                <div class="sell">
                  <p>
                    <img src="../../assets/images/满减.png" alt="">
                    <span>满25减11|满40减18|满60减22</span>
                  </p>
                  <p>
                    <img src="../../assets/images/折扣.png" alt="">
                    <span>折扣商品5折起</span>
                  </p>
                </div>
              </div>
            </div>
          </li>
          <li>
            <div class="restayrant">
              <div class="res-img">
                <img src="../../assets/images/9.jpg" alt="">
              </div>
              <div class="res-dec">
                <h3>肯德基(城东广场店)</h3>
                <div class="start">
                  <div class="left"><start :score='4.7'></start><span class="score">4.7</span><span class="num">月售6666</span></div>
                  <div class="right">30分钟|1.7km</div>
                </div>
                <div class="send">起送¥10|配送¥4|人均¥19</div>
                <div class="sell">
                  <p>
                    <img src="../../assets/images/满减.png" alt="">
                    <span>满25减11|满40减18|满60减22</span>
                  </p>
                  <p>
                    <img src="../../assets/images/折扣.png" alt="">
                    <span>折扣商品5折起</span>
                  </p>
                </div>
              </div>
            </div>
          </li>
          <li>
            <div class="restayrant">
              <div class="res-img">
                <img src="../../assets/images/7.jpg" alt="">
              </div>
              <div class="res-dec">
                <h3>肯德基(城东广场店)</h3>
                <div class="start">
                  <div class="left"><start :score='4.7'></start><span class="score">4.7</span><span class="num">月售6666</span></div>
                  <div class="right">30分钟|1.7km</div>
                </div>
                <div class="send">起送¥10|配送¥4|人均¥19</div>
                <div class="sell">
                  <p>
                    <img src="../../assets/images/满减.png" alt="">
                    <span>满25减11|满40减18|满60减22</span>
                  </p>
                  <p>
                    <img src="../../assets/images/折扣.png" alt="">
                    <span>折扣商品5折起</span>
                  </p>
                </div>
              </div>
            </div>
          </li>
          <li>
            <div class="restayrant">
              <div class="res-img">
                <img src="../../assets/images/8.jpg" alt="">
              </div>
              <div class="res-dec">
                <h3>肯德基(城东广场店)</h3>
                <div class="start">
                  <div class="left"><start :score='4.7'></start><span class="score">4.7</span><span class="num">月售6666</span></div>
                  <div class="right">30分钟|1.7km</div>
                </div>
                <div class="send">起送¥10|配送¥4|人均¥19</div>
                <div class="sell">
                  <p>
                    <img src="../../assets/images/满减.png" alt="">
                    <span>满25减11|满40减18|满60减22</span>
                  </p>
                  <p>
                    <img src="../../assets/images/折扣.png" alt="">
                    <span>折扣商品5折起</span>
                  </p>
                </div>
              </div>
            </div>
          </li>
        </ul>       
      </div>
      </div>
      <van-tabbar active-color="#ffc540" v-model="active">
        <van-tabbar-item icon="home-o">首页</van-tabbar-item>
        <van-tabbar-item icon="search">订单</van-tabbar-item>
        <van-tabbar-item icon="setting-o">我的</van-tabbar-item>
      </van-tabbar>     
  </div>
</template>

<script>
import Vue from 'vue'
import start from '../star/Star'
import BScroll from 'better-scroll'
import { Tabbar, TabbarItem } from 'vant';
Vue.use(Tabbar).use(TabbarItem);
export default {
    name:'Index',
    components:{start},
    data(){
      return {flag:true,isActive:true,active: 0}
    },
    props:{
      currentCity:String
    },
    methods:{
      initScroll(){
        window.addEventListener('scroll',()=>{
          let Y=document.documentElement.scrollTop
          if(Y>196){
            this.flag=false
            this.isActive=false
          }else if(Y>0&&Y<196){
            this.flag=true
            this.isActive=true
          }
        },false); 
      },
    },
    created(){
      this.$nextTick(() => {
        this.initScroll()  
      })    
    },

}
</script>

<style scoped>
/* v-enter 【这是一个时间点】 是进入之前，元素的起始状态，此时还没有开始进入 */
    /* v-leave-to 【这是一个时间点】 是动画离开之后，离开的终止状态，此时，元素 动画已经结束了 */
    .v-enter,
    .v-leave-to {
      transform: translateX(-50px);
    }
    /* v-enter-active 【入场动画的时间段】 */
    /* v-leave-active 【离场动画的时间段】 */
    .v-enter-active,
    .v-leave-active{
      transition-duration: 300ms;
      transition-timing-function: linear;
    }
  .header{
    position: fixed;
    top:0;
    left:0;
    right: 0;
    height: 50px;
    padding: 0 10px;
    background-color: black;
    display: flex;
    align-items: center;
    z-index: 15;
  }
  .address{
    line-height: 30px;
    display: flex;
    align-items: center;
    max-width: 200px;
    flex-shrink: 0;
  }
  .address>img{
    width: 20px;
    height: 20px;
  }
  .address>p{
    color: aliceblue;
    font-size: 16px;
    margin-left: 5px;
  }
  .search{
    flex: 1 0 0;
    background-color: #fff;
    border-radius: 100px;
    position: relative;
    margin-left: 20px;
    overflow: hidden;
  }
  .search>img{
    width: 20px;
    height: 20px;
    margin: 0 10px;
    position:absolute;
    z-index: 16;
    left: 0;
    top:20%;
  }
  .search>input{
   height: 30px;
   width: 100%;
   opacity: 1;
   position: relative;
   line-height: 30px;
   border: none;
   box-sizing: border-box;
   overflow: hidden;
   text-overflow: ellipsis;
   padding:0 30px;
  }
  .icons{
    margin-top: 50px;
    padding: 15px;
    overflow: hidden;
  }
  .icons-item:nth-child(1){
    margin-bottom: 18px;
  }
  .icons-item{
    display: flex;
    justify-content:space-between;
    
  }
  .icons-wrapper{
    width: 44px;
    position: relative;
    text-decoration: none;
  }
  .icons-img{
    height: 44px;
    width: 44px;
  }
  .icons-img>img{
    width: 100%;
    height: 100%;
  }
  .icons-dec{
    text-align: center;
    color: #333;
    font-size: 11px;
    margin-top: 8px;
  }
  .seller{
    text-align: center;
    margin-bottom: 8px;
  }
  .classify{
    height: 40px;
    width: 100%;
    position: relative;
    border-top: 0.3px solid #ccc;
    border-bottom: 0.3px solid #ccc;
  }
  ._classify{
    height: 40px;
    width: 100%;
    position: fixed;
    top:50px;
    background: #fff;
    border-top: 0.3px solid #ccc;
    border-bottom: 0.3px solid #ccc;
    z-index: 22;
  }
  .classify>ul{
    display: flex;
    justify-content: space-between;
    list-style: none;
  }
  .classify>ul>li{
    line-height: 40px;
    width: 24%;
    text-align: center;
    font-size: 14px;
    color: #666;
  }
  .classify .active{
    font-weight: 700;
    color: #333333;
  }
  ._classify>ul{
    list-style: none;
    display: flex;
    justify-content: space-between;
  }
  ._classify>ul>li{
    line-height: 40px;
    width: 24%;
    display: inline-block;
    text-align: center;
    font-size: 14px;
    color: #666;
  }
  ._classify .active{
    font-weight: 700;
    color: #333333;
  }
  .restayrant{
    position: relative;
    margin: 10px;
    display: flex;
    flex-direction: row;
  }
  .res-img{
    width: 76px;
    height: 57px;
    box-sizing: border-box;
    border: 0.5px solid #eee;
  }
  .res-img>img{
    width: 100%;
    height: 100%;
  }
  .res-dec{
    flex:1 0 0;
    margin-left: 10px;
  }
  .res-dec>h3{
    font-size: 16px;
    color:#333;
    font-weight: 550;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .start{
    margin-top: 5px;
    display: flex;
    line-height: 1.4;
  }
  .left{
    display: flex;
    font-size: 11px;
    color: #333;
    line-height: 1;
  }
  .score{
    margin:0 5px;
  }
  .right{
    flex: 1 0 0;
    text-align: right;
    font-size: 11px;
    color: #333;
    line-height: 1;
  }
  .send{
    font-size: 11px;
    color: #333;
    line-height: 1.4;
    margin-top: 8px;
  }
  .sell{
    display: flex;
    flex-direction: column;
    margin-top: 8px;
  }
  .sell p{
    display: flex;
    margin-bottom: 5px;
  }
  .sell img{
    width: 15px;
    height: 15px;
  }
  .sell span{
    font-size: 11px;
    color: #333;
    height: 15px;
    display: inline-block;
    line-height: 15px;
    margin-left: 5px;
  }
</style>