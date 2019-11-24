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
       <i-card  v-for="item in top" :key="item" i-class="split" extra="item.name" :thumb="item.image">
          <view slot="content">{{item.reason}}</view>
         <view slot="footer">{{item.type}}</view>
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
        top:[
      {"name":"少年的你","type":"类型：剧情/犯罪/爱情","image":"/static/images/少年的你.jpg","reason":"推荐理由"},
      {"name":"我和我的祖国","type":"类型：剧情","image":"/static/images/我和我的祖国.jpeg","reason":"推荐理由"},
      {"name":"中国机长","type":"类型：剧情/灾难","image":"/static/images/中国机长.jpg","reason":"推荐理由"},
      {"name":"冰雪奇缘2","type":"类型：动画/喜剧/冒险/美国","image":"/static/images/冰雪奇缘2.jpg","reason":"推荐理由"},
      {"name":"海上钢琴师","type":"类型：剧情/音乐/意大利","image":"/static/images/海上钢琴师.jpg","reason":"推荐理由"},
    
      ]
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
