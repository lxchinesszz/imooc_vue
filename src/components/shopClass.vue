<template>

    <el-card :body-style="{ padding: '0px' }" class="elCard"  >
      <img :src="shopClassImgUrl" class="image">
      <div style="padding: 14px;">
        <span>好吃的汉堡</span>
        <div class="bottom clearfix">
          <time class="time">{{ currentDate }}</time>
          <el-button type="text" class="button">操作按钮</el-button>
        </div>
      </div>
    </el-card>

</template>

<script>
export default {
  name: 'shopClass',
  props: ['shopClassImgUrl'],
  data () {
    return {
      currentDate: new Date()
    }
  }
}
</script>

<style scoped>

.elCard{
  width: 280px;
  height: 300px;
  display: block;
  float: left;
  margin-right: 5px;
  border-radius: 10px;
}
.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
}

.button {
  padding: 0;
  float: right;
}

.image {
  width: 100%;
  display: block;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}

.clearfix:after {
  clear: both
}
</style>
