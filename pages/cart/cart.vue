<template>
  <view>
    <view style="height: 93vh; overflow-y: scroll;">
      <van-card v-for="(index,item) in [1,2,3,4,5,6]"
        :key="index"
        num="3"
        tag="标签"
        price="10.00"
        desc="IPad平板超值"
        title="IPad平板"
        thumb="https://img01.yzcdn.cn/vant/ipad.jpeg"
      >
        <view slot="footer">
          <van-icon name="clear" size="20px"/>
          <van-icon name="add" size="20px"/>
        </view>
      </van-card>
    </view>
    
   <view class="submit">
    <van-submit-bar
      :price="3050"
      button-text="提交订单"
      :safe-area-inset-bottom="false"
    />
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
      onSubmit(){
        alert("提交成功")
      }
      
    }
  }
</script>

<style>
  .submit{
    position: fixed;
    bottom: 0;
  }

</style>
