<template>
  <el-container>
    <div>
      <Applogo></Applogo>
    </div>
    <el-header>
      <el-menu :default-active="activeIndex" mode="horizontal" router>
        <el-menu-item index="/">网站首页</el-menu-item>
        <el-menu-item index="/news">新闻动态</el-menu-item>
        <el-menu-item index="/tab/tech">产品中心</el-menu-item>
        <el-menu-item index="/tab/solution">解决方案</el-menu-item>
        <el-menu-item index="/tab/play">成功案例</el-menu-item>
        <el-menu-item index="/tab/apple">营销服务</el-menu-item>
        <el-menu-item index="/tab/play1">人才招聘</el-menu-item>
        <el-menu-item index="/about/inasdf">关于我们</el-menu-item>
        <el-menu-item index="/linkme">联系我们</el-menu-item>
      </el-menu>
    </el-header>
    <el-main>
      <nuxt keep-alive />
    </el-main>
    <el-footer>
      <footer>
        <div>
          <div class="footerList">
            <div class="footerListTitle">
              <a href="">新闻动态</a>
            </div>
            <span>
              <a href="">公司新闻</a>
            </span>
            <span>
              <a href="">行业资讯</a>
            </span>
            <span>
              <a href="">展会信息</a>
            </span>
          </div>
          <div class="footerList">
            <div class="footerListTitle">
              <a href="">产品中心</a>
            </div>
            <span>
              <a href="">水联网产品</a>
            </span>
            <span>
              <a href="">气联网系列</a>
            </span>
            <span></span>
          </div>
          <div class="footerList">
            <div class="footerListTitle">
              <a href="">解决方案</a>
            </div>
            <span>
              <a href="">智慧城市水系统</a>
            </span>
            <span>
              <a href="">成功案例</a>
            </span>
            <span></span>
          </div>
          <div class="footerList">
            <div class="footerListTitle">
              <a href="">营销与服务</a>
            </div>
            <span>
              <a href="">服务政策</a>
            </span>
            <span>
              <a href="">下载中心</a>
            </span>
            <span>
              <a href="">问题反馈</a>
            </span>
          </div>
          <div class="footerList">
            <div class="footerListTitle">
              <a href="">关于我们</a>
            </div>
            <span>
              <a href="">公司信息</a>
            </span>
            <span>
              <a href="">资质荣耀</a>
            </span>
            <span>
              <a href="">人力资源</a>
            </span>
          </div>
          <div class="footerList">
            <div class="QRcode">
              <img src="~assets/img/qrcode.jpg" alt="">
            </div>
          </div>
          <div class="footerList">
            <div class="footerListTitle">
              <a href="">解决方案</a>
            </div>
            <span>智慧城市水系统</span>
            <span>成功案例</span>
            <span></span>
          </div>
        </div>
        <div class="footerInfo">
          <span>水联网_海绵城市监测评价体系_城市水文_排水信息化_城市水系统信息化解决方案 | 城市水系统信息化技术服务商</span>
        </div>
      </footer>
    </el-footer>
  </el-container>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: "/"
    };
  },
  created() {
    this.activeIndex = this.$route.path;
  }
};
</script>
<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI",
    Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}
.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
<<<<<<< HEAD

.el-menu--horizontal>.el-menu-item {
    float: left;
    height: 100px !important;
    line-height: 100px !important;
    padding: 0 20px;
    font-size: 16px;
    color: #333;
}
.el-header {
    padding: 0;
    height: 100px !important;
    position: fixed;
    width: 100%;
    display: flex;
    justify-content: center;
    background-color: white;
    z-index: 999;
}
.el-menu--horizontal {
    width: 100%;
    display: flex;
    justify-content: center;
}
.el-main{
=======
.el-header {
>>>>>>> 8c827ee14373ebae719fd8c133d78a36814019a5
  padding: 0;
}
.el-footer {
  padding: 0;
}
/*footer样式*/
a {
  color: white;
}
footer > div:nth-child(1) {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  height: 220px;
  background: #222;
  color: white;
  padding: 55px 300px;
}
.footerList {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  width: 11%;
}
.footerList > span {
  font-size: 12px;
  color: #fff;
  margin-bottom: 10px;
}
.footerListTitle {
  font-size: 14px;
  color: #fff;
  margin-bottom: 20px;
  font-weight: bold;
}
.QRcode > img {
  width: 100px;
  height: 100px;
}
footer > div:nth-child(2) {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60px;
  background: #111;
  color: white;
}
</style>

