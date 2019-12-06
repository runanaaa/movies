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
<i-panel title="全部">
    <view style="padding: 15px;">
      <i-card  v-for="item in top" :key="item"  i-class="split" :extra="item.name" :thumb="item.image">
         <view slot="content">推荐原因：{{item.reason}}</view>
         <view slot="footer">类型：{{item.type}}</view>
      </i-card>
    </view>
</i-panel>
  </div>
</template>
<script>
import card from '@/components/card'
import information from '@/data/information.json'
export default {
  data () {
    return {
      grids:[
        {title:"最新",image:"/static/images/1.png","url":'../list/main?mole=1'},
        {title:"内地",image:"/static/images/2.png","url":'../list/main?mold=2'},
        {title:"中国香港",image:"/static/images/2.png","url":'../list/main?mold=3'},
        {title:"中国台湾",image:"/static/images/2.png","url":'../list/main?mold=4'},
      ],
    top:information,
     
      components: {
      card
       },
      
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