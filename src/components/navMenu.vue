<template>
  <el-menu :default-active="activeIndex" class="el-menu-demo case-content" mode="horizontal" @select="handleSelect">
    <el-menu-item index="1" style="width: 200px">
      <img src="https://www.imooc.com/static/img/index/logo.png" >
    </el-menu-item>
    <el-menu-item index="2" class="nav">免费课程</el-menu-item>

    <el-menu-item index="3" class="nav">实战课程</el-menu-item>

    <el-menu-item index="4" class="nav">就业班</el-menu-item>

    <el-menu-item index="5" class="nav">猿问</el-menu-item>

    <el-menu-item index="6" class="nav">手办</el-menu-item>

    <el-menu-item index="7" class="nav">猿聘</el-menu-item>

    <el-menu-item class="nav">
      <el-autocomplete
        placeholder="前端入门 Java基础"
        clearable = 'false'
       >
        <i
          class="el-icon-search"
          slot="suffix"
        >
        </i>

      </el-autocomplete>
    </el-menu-item>

    <el-menu-item index="8" class="nav" style="margin-left: 100px;margin-right: 0px">下载APP</el-menu-item>

    <el-menu-item index="9" class="nav" >
      <el-button icon="el-icon-goods" round>购物车</el-button>
    </el-menu-item>

    <el-menu-item index="10" class="nav">登录</el-menu-item>

    <el-menu-item index='11' class="nav">注册</el-menu-item>
  </el-menu>
</template>

<script>

export default {

}
</script>

<style scoped>
.el-menu-demo{
  height: 75px;
  -webkit-box-shadow: 0 0 20px #d1c7e7;
  -moz-box-shadow: 0 0 20px #d1c7e7;
  box-shadow: 0 0 20px #d1c7e7;
  -o-box-shadow:0 0 20px #d1c7e7);
  /*border-radius: 100px/10px;*/
}
.nav{
  margin-top: 10px;
  color: #29333c;
}
</style>
