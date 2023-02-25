<template>
  <view>
    <view class="goodInfo">
      <!-- 轮播图 -->
      <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" :circular="true">
        <!-- 循环渲染轮播图的 item 项 -->
        <swiper-item v-for="(item, i) in [1,2,3,4]" :key="i">
          <view class="swiperItem">
            {{item}}
          </view>
        </swiper-item>
      </swiper>
      
      <!-- 图片展示 -->
      <viwe class="showImg">
        <van-image width="300" height="300" src="https://img.yzcdn.cn/vant/cat.jpeg" v-for="(item, i) in [1,2,3,4]" :key="i"/>
      </viwe>
    </view>

    
    
    
    
    <view class="buyGood">
      <van-goods-action>
        <van-goods-action-icon icon="chat-o" text="客服" dot />
        <van-goods-action-icon icon="cart-o" text="购物车" info="5" />
        <van-goods-action-button text="加入购物车" type="warning" />
        <van-goods-action-button text="立即购买" />
      </van-goods-action>
    </view>
    
    
  </view>
</template>

<script>
  export default {
    data() {
      return {
        
      }
    },
    methods: {
      
    }
  }
</script>

<style>
  .swiperItem{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
  }
  
  .goodInfo{
    height: 90vh;
    width: 100vw;
  }
  
  
  .buyGood{
    height: 10vh;
    width: 100vw;
  }
  
  .showImg{
    display: flex;
    align-items: center;
    height: max-content;
    flex-direction: column;
  }

</style>
