<template>
  <view class="mainBox">
    <!-- 添加信息按钮 -->
    <van-icon name="add" size="50px" class="addButton" color="#056de8" />
    
    <view class="communityCard" v-for="(index,item) in [1,2,3,4]" :key="index">
      <view class="userInfo">
        <van-icon name="user-circle-o" size="30px" class="userHead"/>
        <view class="userText">
          <h4>剪纸王</h4>
          <span>2022/19/19 · <span style="color: aquamarine; margin: 0 5px;">剪纸杂谈</span></span>
        </view>
      </view>
      <view class="textInfo">
        <h3>剪纸在生活中变的越来越重要了</h3>
        <span>中国剪纸是一种用剪刀或刻刀在纸上剪在纸...</span>
      </view>
      
      <van-image width="200" height="200" src="https://img.yzcdn.cn/vant/cat.jpeg" class="img" />
      
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
  .addButton{
    background-color: white;
    position: fixed;
    bottom: 30px;
    right: 30px;
  }
  
  .mainBox{
    background-color: #f8f8f8;
    height: 100vh;
    width: 100vw;
    overflow-y: scroll;
  }
  
  
  .communityCard{
    margin-bottom: 8px;
    box-sizing: border-box;
    height: max-content;
    width: 100%;
    background-color: white;
    padding: 10px 10px;
  }
  
  .userInfo{
    display: flex;
    height: 20%;
    width: max-content;
  }
  
  .userInfo .userText{
    display: flex;
    flex-direction: column;
  }
  
  .userHead{
    margin: 3px 3px;
  }
  
  .textInfo{
    width: 100%;
    padding: 10px;
  }
  .textInfo h3{
    font-weight: blod;
    font-size: 20px;
  }
  
  .img{
    padding: 10px;
  }
</style>
