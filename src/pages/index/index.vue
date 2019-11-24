<template>
  <div>
    <swiper
      :indicator-dots="indicatorDots"
      :autoplay="autoplay"
      :interval="interval"
      :duration="duration"
      style="height:200px"
    >
    <block v-for="item in imgUrls" :key="item">
      <swiper-item>
        <image :src="item" style="width:100%;" />
      </swiper-item>
    </block>
  </swiper>
  <i-panel v-for="item in recommand" :key="item">
      <view class="setting">
        <image :src='item.image' style="width:130rpx;height:180rpx;"/>
        <text style="padding:7px;line-height:17px">
          <text class="movie">{{item.name}}</text>
          <text class="type">\n{{item.type}}</text>
          <text class="actor">\n演员:{{item.actor}}</text> 
        </text>
        <button class="button" @click='jump(item)'>查看电影详情</button>
      </view>
    </i-panel>
  
  </div>
</template>
<script>
import card from '@/components/card'
import top from '@/data/top.json'      
export default {
  data () {
    return {
      title_name:"热门",
      grids:[
        {title:" ",image:" "},
        {title:" ",image:" "},
        {title:" ",image:" "},
        {title:" ",image:" "},
      ],
       imgUrls: [
        '/static/images/少年的你.jpg',
        '/static/images/我和我的祖国.jpeg',
        '/static/images/中国机长.jpg'
      ],
      indicatorDots: true,
      autoplay: true,
      interval: 5000,
      duration: 1000,
      recommand:top,
      components: {
      card
       },
         
    }
  },
  methods: {
      goToJump(url){
      wx.navigateTo({url})
    },
    jump(item){
    wx.navigateTo({
       url:'../detail/main?id='+item.id+'&name='+item.name+'&actor='+item.actor+'&type='+item.type+
       '&image='+item.image+'&introduce='+item.introduce
    })
    }

  },
 
  created () {
  }
}
</script>

<style scoped>
div >>> .no-border {
  border-width: 0pt;
}
.movie{
  color:black;
  font-size: 36rpx;
  font-family:microsoft yahei;
  font-weight:normal;
  letter-spacing:1.5px;
}
.type{
  color:#696969;
  font-size:28rpx; 
  font-weight:normal;
}
.actor{
  color:#696969;
  font-size:28rpx;
  font-family:microsoft yahei; 
}
.button{
  position: absolute;
  right: 12px;
  top: 32px;
  font-size:14px;
  background-color:#3bb3e0;
  color:white;
  margin:2.5px
}
.setting{
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-left:9px;
  margin-top: 4px;
}
.left{
  float:left;
  width:3rem;
  height:1rem;
  background-color:red;
}

.right{
  float:left;
  width:4.5rem;
  height:1rem;
  background-color:green;
}
</style>
