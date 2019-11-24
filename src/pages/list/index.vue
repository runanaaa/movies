<template>
  <div>
     <i-card v-for="item in list" :key="item" i-class="split" :extra="item.name" :thumb="item.image">
         <view slot="content">推荐原因：{{item.reason}}</view>
         <view slot="footer">类型：{{item.type}}</view>
      </i-card>
  </div>
</template>
<script>              
export default {
  data () {
    return {
      list:[]
    }
  },
  onLoad(option){
    console.log(option.type)
    this.list=require('@/data/'+option.type+'.json')
    console.log(this.list)
  },
  methods: {
    },
  created () {
  }
}
</script>
<style scoped>
div >>> .split {
  margin-bottom: 10pt;
}
</style>