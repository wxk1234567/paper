<template>
  <view>
    <van-sticky>
      <!-- 搜索框 -->
      <van-search
        v-model="search"
        shape="round"
        background="#e06c61"
        placeholder="请输入搜索关键词"
        class="searchBar"
      />
      <van-icon class="scanIcon" name="scan"/>
    </van-sticky>

    <!-- 轮播图 -->
    <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" :circular="true">
      <!-- 循环渲染轮播图的 item 项 -->
      <swiper-item v-for="(item, i) in itemList" :key="i">
        <view class="swiperItem">
          {{item}}
        </view>
      </swiper-item>
    </swiper>
    
    <!-- 首页商品分类 -->
    <van-grid>
      <van-grid-item icon="photo-o" text="文字" />
      <van-grid-item icon="photo-o" text="文字" />
      <van-grid-item icon="photo-o" text="文字" />
      <van-grid-item icon="photo-o" text="文字" />
      <van-grid-item icon="photo-o" text="文字" />
      <van-grid-item icon="photo-o" text="文字" />
      <van-grid-item icon="photo-o" text="文字" />
      <van-grid-item icon="photo-o" text="文字" />
    </van-grid>
    
    <!-- 首页商品展示 -->
    <van-grid column-num="2" border center>
      <van-grid-item use-slot v-for="(item,index) in [1,2,3,4,5,6]" :key="index">
        <div class="goodCards" @click="toGoodDetail">
          <img
            style="width: 100%; height: 150px;"
            :src="`https://img.yzcdn.cn/vant/apple-${ index + 1 }.jpg`"
          />
          <div class="goodText">
            <span class="money">￥368</span>
            <span class="goodName">国画剪纸</span>
            <van-icon class="addIcon" color="white" name="plus" />
          </div>
        </div>
      </van-grid-item>
    </van-grid>

  </view>
</template>

<script>
  export default {
    data() {
      return {
        search:"",
        itemList:[1,2,3]
      }
    },
    methods: {
      toGoodDetail(){
        // 跳转到商品详情页面
        wx.navigateTo({
          url: '/pages/goodDetail/goodDetail'
        })
      }
      
    }
  }
</script>

<style>
  .searchBar{
    height: 54px;
  }
  .swiperItem{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
  }
  .scanIcon{
    width: 50px;
    height: 54px;
    position: absolute;
    top: 0px;
    right: 0px;
    z-index: 99;
  }
  .goodCards{
    width: 100%;
    height: 200px;
  }
  .goodText{
    position: relative;
    display: flex;
    flex-direction: column;
  }
  .money{
    font-weight: bold;
    font-size: 1.2rem;
  }
  .addIcon{
    position: absolute;
    bottom: 0;
    right: 0;
    width: 30px;
    height: 30px;
    border-top-left-radius: 18px;
    background-color: black;
  }
</style>
