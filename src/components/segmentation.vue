<template>
<div class="segment">
  <span class="el-icon-loading"  style="color: red"></span>
  {{segmentText}}
  <span class="el-icon-loading" style="color: red"></span>
</div>
</template>

<script>
export default {
  props: [ 'segmentText' ]
}
</script>

<style scoped>
.segment{
  color: dimgray;
  font-size: 20px;
}
</style>
