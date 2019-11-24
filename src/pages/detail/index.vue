<template>
  <div >
    <i-panel>
      <view class='header-container'>
        <image class='bg' :src='option.image'/>
        <view class='setting'>
          <image :src='option.image' style="width:250rpx;height:360rpx;"/>
          <text style="padding:8px;line-height:30px">
            <text class="movie">{{option.name}}</text>
            <text class="type">\n类型:{{option.type}}</text>
            <text class="actor">\n演员:{{option.actor}}</text> 
          </text>
        </view>
      </view>     
    </i-panel>

    <i-panel style="margin-top:2px">
     <view  class="li"  @click='changeToggle'>
        <view  style="padding:8px;line-height:30px"  class='introduce'>剧情简介：{{option.introduce}}</view>
       
    </view>
    </i-panel>
  </div>
</template>

<script>

export default {
  methods: {
  },
   data:{
    option:[],
  },
  onLoad(option){
   this.option=option;
   console.log(option)
  }
}
</script>
<style>
.li {
  background-color: #fff;
  display: flex;
  justify-content: space-between;
  font-size: 10rpx;
  width: 100%;
  padding: 0 4%;
  height: 500px;
  line-height: 100rpx;
  border-bottom: 1rpx solid #f1f1f1;
}
.movie{
  color:white;
  font-size: 45rpx;
  font-family:microsoft yahei;
  font-weight:normal;
  letter-spacing:1.5px;
}
.type{
  color:#D3D3D3;
  font-size:32rpx; 
  font-weight:normal;
}
.actor{
  color:#D3D3D3;
  font-size:32rpx;
  font-family:microsoft yahei; 
}
.setting{
  width: 750rpx;
  height: 450rpx;
  color: rgb(213, 214, 210);
  position: absolute;
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-left: 15px;
}
.header-container {
  display: flex;
  flex-direction: row;
  height: 450rpx;
  background-color: #fff;
  align-items: center;
  position: relative; 
}
.bg{
filter: blur(9px);
width: 100%;
height: 100%;
}
.introduce{
  font-size: 30rpx;
  color:#696969;
  margin-left: 20px;
  margin-right: 20px;

}
</style>
