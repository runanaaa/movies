<template>
  <div>
     <i-grid i-class="no-border">
    <i-grid-item @click="goType(grid)" v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image :src="grid.image" />
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
    </i-grid-item>
</i-grid>
 <i-panel >
    <view style="padding: 15px;">
      <i-card v-for="item in top" :key="item" i-class="split" :extra="item.name" :thumb="item.image">
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
      grids:[
        {title:"最新",image:"/static/images/1.png"},
        {title:"内地",image:"/static/images/2.png"},
        {title:"中国香港",image:"/static/images/2.png"},
        {title:"中国台湾",image:"/static/images/2.png"},
      ],
    top:[
      {"name":"南方车站的聚会","type":"类型：剧情/犯罪","image":"/static/images/南方车站的聚会.jpg","reason":"推荐理由"},
      {"name":"你是凶手","type":"类型：剧情/犯罪/悬疑","image":"/static/images/你是凶手.jpg","reason":"推荐理由"},
      {"name":"长安道","type":"类型：剧情/犯罪/悬疑","image":"/static/images/长安道.jpg","reason":"推荐理由"},
      {"name":"大约在冬季","type":"类型：剧情/爱情","image":"/static/images/大约在冬季.jpg","reason":"推荐理由"},
      {"name":"小小的愿望","type":"类型：剧情/喜剧","image":"/static/images/小小的愿望.jpg","reason":"推荐理由"},
      {"name":"受益人","type":"类型：剧情/喜剧/爱情","image":"/static/images/受益人.jpg","reason":"推荐理由"},
      {"name":"海角七号","type":"类型：剧情/爱情/喜剧","image":"/static/images/海角七号.jpg","reason":"推荐理由"},
      {"name":"那些年我们一起追过的女孩","type":"类型：剧情/喜剧/爱情","image":"/static/images/那些年我们一起追过的女孩.jpg","reason":"推荐理由"},
      {"name":"我的少女时代","type":"类型：喜剧/爱情","image":"/static/images/我的少女时代.jpg","reason":"推荐理由"},
      {"name":"犯罪现场","type":"类型:犯罪/悬疑/惊悚","image":"/static/images/犯罪现场.jpg","reason":"推荐理由1"},
      {"name":"大追捕","type":"类型:剧情/动作/犯罪","image":"/static/images/大追捕.jpg","reason":"推荐理由1"},
      {"name":"小Q","type":"类型:剧情","image":"/static/images/小Q.jpg","reason":"推荐理由1"}
      ]
    }
  },
  methods: {
    goType(type){
       console.log(type)
       let url='../list/main?type='+type.title
       mpvue.navigateTo({ url })
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
div >>> .split {
  margin-bottom: 10pt;
}
</style>