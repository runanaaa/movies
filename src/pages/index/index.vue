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
        <image :src="item" style="width:100%;"/>
      </swiper-item>
    </block>
  </swiper>
   <i-panel :title="title_name">
    <view style="padding: 15px;">
       <i-card i-class="split" extra="少年的你" thumb="/static/images/少年的你.jpg">
         <view slot="content">推荐理由</view>
         <view slot="footer">类型：剧情/爱情/犯罪</view>
      </i-card>
      <i-card i-class="split" extra="我和我的祖国" thumb="/static/images/我和我的祖国.jpeg">
         <view slot="content">推荐理由</view>
         <view slot="footer">类型：剧情</view>
      </i-card>
      <i-card i-class="split" extra="中国机长"  thumb="/static/images/中国机长.jpg">
         <view slot="content">推荐理由</view>
         <view slot="footer">类型：剧情/灾难</view>
      </i-card>
      <i-card i-class="split" extra="冰雪奇缘2"  thumb="/static/images/冰雪奇缘2.jpg">
         <view slot="content">推荐理由</view>
         <view slot="footer">类型：动画/喜剧/冒险/美国</view>
      </i-card>
       <i-card i-class="split" extra="海上钢琴师"  thumb="/static/images/海上钢琴师.jpg">
         <view slot="content">推荐理由</view>
         <view slot="footer">类型：剧情/音乐/意大利</view>
      </i-card>
    </view>
</i-panel>
  </div>
</template>
<script>
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
    }
  },
  methods: {
    },
  created () {
  }
}
</script>

<style scoped>
</style>
