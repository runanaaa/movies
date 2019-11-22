<template>
  <div>
     <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/1.png" />
        </i-grid-icon>
        <i-grid-label>最新</i-grid-label>
    </i-grid-item>
   <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/2.png" />
        </i-grid-icon>
        <i-grid-label>内地</i-grid-label>
    </i-grid-item>
     <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/2.png" />
        </i-grid-icon>
        <i-grid-label>中国香港</i-grid-label>
    </i-grid-item>
     <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/2.png" />
        </i-grid-icon>
        <i-grid-label>中国台湾</i-grid-label>
    </i-grid-item>
</i-grid>
  </div>
</template>
<script>
export default {
  data () {
    return {
    }
  },
  methods: {
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