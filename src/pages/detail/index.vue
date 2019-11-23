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
      {name:"电影名1",type:"类型1",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",reason:"推荐理由1"},
      {name:"电影名2",type:"类型2",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",reason:"推荐理由1"},
      {name:"电影名3",type:"类型3",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",reason:"推荐理由1"}
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