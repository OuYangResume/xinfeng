<template>
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
          <span style="font-size:14px;">水联网_海绵城市监测评价体系_城市水文_排水信息化_城市水系统信息化解决方案 | 城市水系统信息化技术服务商</span>
        </div>
      </footer>
</template>
<script>
export default {
    
}
</script>
<style scoped>
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
