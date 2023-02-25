<template>
  <view class="box">
    <view class="aside">
      <van-sidebar active-key="0">
        <van-sidebar-item title="人物类型" />
        <van-sidebar-item title="鸟兽类型" />
        <van-sidebar-item title="文字类型" />
        <van-sidebar-item title="器用类型" />
        <van-sidebar-item title="鳞介类型" />
        <van-sidebar-item title="花木类型" />
        <van-sidebar-item title="果菜类型" />
        <van-sidebar-item title="昆虫类型" />
        <van-sidebar-item title="山水类型" />
      </van-sidebar>
    </view>
    
    <view class="mainView">
      <van-card
        v-for="(item,index) in [1,2,3,4,5,6,7,8]"
        :key="index"
        num="2"
        price="2.00"
        desc="描述信息"
        title="商品标题"
        :thumb="`https://img.yzcdn.cn/vant/apple-${ index + 1 }.jpg`"
      />
    </view>
    
  </view>
</template>

<script>
  export default {
    data() {
      return {
        activeKey: 0,
      }
    },
    methods: {
      
    }
  }
</script>

<style scoped>
  /* 定义sidebar的宽度*/
 :root {
    --sidebar-width:30vw;
  }
  .box{
    display: flex;
  }
  .aside{
    height: 100vh;
    width: 30vw;
    background-color: #f7f8fa;
  }
  .mainView{
    height: 100vh;
    width: 70vw;
    overflow: scroll;
  }

</style>
