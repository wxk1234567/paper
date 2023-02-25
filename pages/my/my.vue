<template>
  <view>
    <!-- 顶部选项 -->
    <view class="topBar">
      <div class="text">个人中心</div>
      <van-icon class="seetingIcon" name="setting-o" size="20px"/>
    </view>
    
    <!-- 用户登录 -->
    <view class="login">
      <van-icon name="manager-o" size="60px"/>
      <span>登录 / 注册</span>
    </view>
    
    <!-- 菜单选项 -->
    <view class="usermenu">
      <van-cell-group title="我的订单">
        <van-cell title="查看订单" is-link />
        <van-cell title="待支付" is-link />
        <van-cell title="待收货" is-link />
        <van-cell title="待评价" is-link />
      </van-cell-group>
      <van-cell-group title="其他功能">
        <van-cell title="退出登录" is-link />
      </van-cell-group>

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

<style scoped>
  .topBar{
    height: 54px;
    width: 100%;
    background-color: #e06c61;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .topBar text{
    height: 100%;
    font-weight: blod;
    font-size: 20px;
    line-height: 100%;
    text-align: center;
  }
  .seetingIcon{
    height: 54px;
    width: 54px;
  }
  
  .login{
    width: 100%;
    height: 200px;
    background-color: #e06c61;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }
  .usermenu{
    position: relative;
    top: -20px;
    border-radius: 18px;
    background-color: white;
  }
</style>
