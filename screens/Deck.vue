<template>
  <view class="container">
    <text class="pageTitle">Deck Estimation View</text>


    <scroll-view :style="{width: '100%'}">
      <view class="">

        <view>
          <text-input
          class="ftInput"
        />
        </view>
        
        
      </view>
    </scroll-view>



  </view>
</template>

<script>
export default {
  methods: {
  }
}
</script>

<style>
.pageTitle {
  text-align: center;
  font-size: 30;
  font-weight: bold;
}
.ftInput {
  height: 40;
  width: 300;
  border-color: gray;
  border-width: 1;
}
</style>