<template>
  <el-container style="margin: 35px 145px;" class="bannerCard case-content" >
    <el-aside width="200px" style="height: 400px;background-color: #29333c;   border-top-left-radius: 10px; border-bottom-left-radius: 10px;">

      <el-popover
        placement="left"
        title="标题"
        width="200"
        trigger="hover"
        content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        <el-button class="elbutton" slot="reference" >前沿 / 区块链 / 人工智能</el-button>
      </el-popover>

      <el-popover
        placement="left"
        title="标题"
        width="200"
        trigger="hover"
        content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        <el-button class="elbutton" slot="reference" >前端 / 小程序 / JS</el-button>
      </el-popover>

      <el-popover
        placement="left"
        title="标题"
        width="200"
        trigger="hover"
        content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        <el-button class="elbutton" slot="reference" >后端 / Java / Python</el-button>
      </el-popover>

      <el-popover
        placement="left"
        title="标题"
        width="200"
        trigger="hover"
        content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        <el-button class="elbutton" slot="reference" >移动 / Android / IOS</el-button>
      </el-popover>

      <el-popover
        placement="left"
        title="标题"
        width="200"
        trigger="hover"
        content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        <el-button class="elbutton" slot="reference" >云计算 / 大数据 / 容器</el-button>
      </el-popover>

      <el-popover
        placement="left"
        title="标题"
        width="200"
        trigger="hover"
        content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        <el-button class="elbutton" slot="reference" >运维 / 测试 / 数据库</el-button>
      </el-popover>

      <el-popover
        placement="left"
        title="标题"
        width="200"
        trigger="hover"
        content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        <el-button class="elbutton" slot="reference">后端 / Java / Python</el-button>
      </el-popover>

      <el-popover
        placement="left"
        title="标题"
        width="200"
        trigger="hover"
        content="这是一段内容,这是一段内容,这是一段内容,这是一段内容。">
        <el-button class="elbutton" slot="reference" >UI设计 / 3D动画 / 游戏</el-button>
      </el-popover>

    </el-aside>
    <el-container style="border-radius: 10px;">
      <el-header style="background-color: aquamarine;height: 300px;padding: 0px 0px; border-top-right-radius: 10px;">
        <el-carousel :interval="4000" height="300px" arrow="always" style="border-top-right-radius: 10px;" >
          <el-carousel-item v-for="(srcUrl,index) in srcList" :key="index"  >
            <!--<h3>{{ item }}</h3>-->
            <img :src="srcUrl" style="width: 1000px">
          </el-carousel-item>
        </el-carousel>
      </el-header>
      <el-main style="background-color: white;height: 100px;padding: 0 0; border-bottom-right-radius: 10px;">
        <div class="minShopClass">
          <i class="i-web"></i> <br/>
          Web前端工程师<br/>
          <span>互联网时代最火爆技术</span>
        </div>
        <div class="minShopClass">
          <i class="i-java"></i> <br/>
          Java工程师
          <br/>
          <span>综合就业排名第一</span>
        </div>
        <div class="minShopClass">
          <i class="i-android"></i> <br/>
          Android工程师<br/>
          <span >移动设备市场第一</span>
        </div>
        <div class="minShopClass">
          <i class="i-php"></i> <br/>
          PHP工程师
          <br/>
          <span>世界上最好的语言</span>
        </div>

      </el-main>
    </el-container>
  </el-container>
</template>

<script>
export default {
  data: function () {
    return {
      srcList: ['https://img.mukewang.com/5bd9895e000127ec09360316.jpg', 'https://img.mukewang.com/5bc45ce20001976409360316.jpg', 'https://img.mukewang.com/5bd6e4c60001d96f09360316.jpg']
    }
  }
}

</script>

<style scoped>
  .bannerCard{
    position: relative;
    box-shadow: 0 1px 4px #d5d7d8,0 0 40px #d5d7d8 inset;
    /*border-radius: 100px/10px;*/
    border-radius: 10px;
  }
  .case-content{
    /*border-radius: 100px/10px;*/
    border-radius: 10px;
  }
  .case-content:before ,.case-content:after{
    z-index: -1;
    content: "";
    background-color: #foo;
    position: absolute;
    top: 50%;
    bottom: 0;
    left: 10px;
    right: 10px;
    -webkit-box-shadow: 0 0 20px rgba(0,0,0,0.8);
    -moz-box-shadow: 0 0 20px rgba(0,0,0,0.8);
    box-shadow: 0 0 20px rgba(0,0,0,0.8);
    -o-box-shadow:0 0 20px rgba(0,0,0,0.8);
    border-radius: 100px/10px;
  }

  .elbutton{
    color: darkgrey;
    border: 0px;
    text-align: left;
  }

  .path-banner{

  }
  .minShopClass{
    margin-top: 0px;
    width: 180px;
    height: 100px;
    background-color: white;
    display: block;
    float:left;
    margin-left: 35px;
  }
  .minShopClass>span{
  font-size: 10px;
    color: #959ca2;
  }
  .minShopClass i{
    display: inline-block;
    width: 50px;
    height: 25px;
    background: url("https://www.imooc.com/static/img/index/new/path_new.png") no-repeat;
    background-size: 22px;
    margin-top: 12px;
  }
  .minShopClass .i-php{
    background-position: center -21px;
  }
  .minShopClass .i-web{
    background-position: center 1px;
  }
  .minShopClass .i-java{
    background-position: center -42px;
  }
  .minShopClass .i-android{
    background-position: center -65px;
  }

</style>
