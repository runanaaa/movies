<template>
  <div>
   <i-panel :title="title_name">
    <view style="padding: 15px;">
      <i-card i-class="split" title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
         <view slot="content">内容不错</view>
         <view slot="footer">尾部内容</view>
      </i-card>
      <i-card i-class="split" title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
         <view slot="content">内容不错</view>
         <view slot="footer">尾部内容</view>
      </i-card>
      <i-card i-class="split" title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
         <view slot="content">内容不错</view>
         <view slot="footer">尾部内容</view>
      </i-card>
    </view>
</i-panel>
  </div>
</template>
<script>
export default {
  data () {
    return {
      title_name:"推荐",
      grids:[
        {title:" ",image:" "},
        {title:" ",image:" "},
        {title:" ",image:" "},
        {title:" ",image:" "},
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
