<template>
  <div>
    <div class="lunbo">
      <div class="block">
        <el-carousel trigger="click" height="640px">
          <el-carousel-item v-for="item in imgList" :key="item">
            <h3>
              <img :src="item" alt="" style="width: 100%; height: 100%;">
            </h3>
          </el-carousel-item>
        </el-carousel>
      </div>
    </div>
    <div class="main-solution">
      <TitleMsgShow title="解决方案" titleEN="SOLUTION"></TitleMsgShow>
      <Solution></Solution>
    </div>
    <Classical :classicalExample="classicalExample"></Classical>
    <div class="companyInfo">
      <TitleMsgShow title="公司信息" titleEN="COMPANY INFORMATION"></TitleMsgShow>
      <div style="display: flex;flex-wrap: wrap;justify-content: center;">
        <div class="companyIntroduce" style="margin-right: 50px;">
          <div class="companyIntroduceTitle">
            <span>公司介绍</span>
            <span>COMPANT INTRODUCTION</span>
          </div>
          <div style="width: 614px;">
            <el-card :body-style="{ padding: '0px' }">
              <img src="http://www.newfiber.com.cn/statics/default/images/_gsjjtp.jpg" class="image">
              <div style="padding: 14px;">
                <div class="companyIntroduceInfo">{{companyIntroduce1}}</div>
                <!-- <div class="companyIntroduceInfo">2012年诞生于有世界光谷之称的武汉东湖高新技术开发区，公司位于武汉市东湖新技术开发区光谷大道303号光谷芯中心三期3-11幢1-5层1厂房单元，面积1500平米。公司注册资本1000万元，实收资本1000万元。自创始以来，公司始终坚持走自主创新之路，先后在无源激光测距、可调谐半导体激光吸收 光谱TDLAS、智慧海绵城市监测评价物联网系统开发等技术上有重大研究成果，拥有3项发明专利，50项实用新型专利，24项外观专利，36项软件著作权。2014年公司被认定为“高新技术企业”。2015年10月公司完成股份制改造。2015年12月通过ISO9001-2008质量管理体系认证。2016年7月先后取得信息系统集成资质证书、软企企业证书。2016年被成功认定为“瞪羚企业”。目前公司面向消费者提供的产品包括物联网领域的软、硬件产品、光机电一体化传感器、火灾探测器、气体传感器、水利水文仪器仪表和设备、环境监测治理仪器仪表和设备、气象监测仪器仪表的科研、开发、生产、销售、安装及售后服务；</div> -->
              </div>
            </el-card>
          </div>
        </div>
        <div class="companyNews">
          <div class="companyIntroduceTitle">
            <span>新闻中心</span>
            <span>NEWS CENTER</span>
          </div>
          <div style="width: 614px;">
            <NewsShow :companyNewsList="companyNewsList" :industryInformation="industryInformation" :exhibitionInformation="exhibitionInformation"></NewsShow>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Classical from "../components/Classical";
import TitleMsgShow from "../components/common/TitleMsgShow";
import Solution from "../components/mainpage/Solution";
import NewsShow from "../components/mainpage/NewsShow";
import MsgList from "../components/mainpage/MsgList";

export default {
  data() {
    return {
      companyNews: null,
      companyIntroduce1: null,
      companyNewsList: null,
      industryInformation: null,
      exhibitionInformation: null,
      classicalExample: null,
      imgList: [
        "http://www.newfiber.com.cn/d/file/content/2016/10/581166208bb6a.jpg",
        "http://www.newfiber.com.cn/d/file/content/2017/03/58c73fedd9c0d.jpg",
        "http://www.newfiber.com.cn/d/file/content/2017/03/58c6757a9f44e.jpg"
      ]
    };
  },
  components: {
    Classical,
    TitleMsgShow,
    Solution,
    NewsShow,
    MsgList
  },
  methods: {
    getData() {
      axios
        .get("http://192.168.30.208:9000/XFGD/goPage?pageId=001")
        .then((response) => {
          this.companyIntroduce1 = JSON.parse(response.data.a)[0].content
          this.companyNewsList = JSON.parse(response.data.b).slice(0, 3)
          this.industryInformation = JSON.parse(response.data.c).slice(0, 3)
          this.exhibitionInformation = JSON.parse(response.data.d).slice(0, 3)
          this.classicalExample = JSON.parse(response.data.f).slice(0, 4)
          // console.log(this.companyNewsList);
        })
        .catch(function(error) {
          // handle error
          console.log(error);
        })
        .then(function() {
          // always executed
        });
    }
  },
  created () {
    this.getData()
  }
};
</script>
<style scoped>
.ivu-tabs-bar {
  border: none !important;
}
.topHeader {
  position: fixed;
  top: 0;
  width: 100%;
  background: white;
}
.lunbo {
  margin-top: 101px;
  width: 100%;
  height: 640px;
  background: #005699;
}
.main-solution {
  height: 460px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  background: white;
}
.companyIntroduceTitle {
  margin-bottom: 30px;
}
.companyIntroduceTitle > span:nth-child(1) {
  font-size: 24px;
  font-weight: bold;
  color: #333;
}
.companyIntroduceTitle > span:nth-child(2) {
  margin-left: 30px;
  font-size: 12px;
  color: #666;
}
.companyInfo {
  padding-bottom: 50px;
  background: white;
}
.image {
  width: 100%;
  height: 450px;
  display: block;
}
.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}
.companyIntroduceInfo {
  position: relative;
  line-height: 24px;
  /* 3 times the line-height to show 3 lines */
  height: 96px;
  overflow: hidden;
}
.companyIntroduceInfo::after {
  content: "...";
  font-weight: bold;
  position: absolute;
  bottom: 0;
  right: 0;
  padding: 0 20px 1px 45px;
  background: url(http://css88.b0.upaiyun.com/css88/2014/09/ellipsis_bg.png)
    repeat-y;
}
</style>






