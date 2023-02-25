<template>
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
</template>

<script>
</script>

<style>
  .searchBar{
    height: 54px;
  }
  .scanIcon{
    width: 50px;
    height: 54px;
    position: absolute;
    top: 0px;
    right: 0px;
    z-index: 99;
  }
</style>