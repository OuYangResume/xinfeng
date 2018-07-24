<template>
    <div class="aboutMain">

        <div class="about-head">
            <TitleMsgShow title="关于我们" titleEN="ABOUT US" titleBackground="123"></TitleMsgShow>
        </div>
        <el-row>
            <el-col :span="24">
                <div>
                    <el-tabs v-model="activeName" @tab-click="handleClick">
                        <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
                        <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
                        <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
                        <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
                    </el-tabs>
                </div>
            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                <TitleMsgShow title="公司介绍" titleEN="COMPANY INTRODUCTION"></TitleMsgShow>
                <div class="about-conent">
                    <div class="about-company">
                        <div class="companyInfo">
                            2012年诞生于有世界光谷之称的武汉东湖高新技术开发区， 公司位于武汉市东湖新技术开发区光谷大道303号光谷芯中心三期3-11幢1-5层1厂房单元， 面积1500平米。公司注册资本1000万元，实收资本1000万元。自创始以来，公司始终坚持走自主创新之路， 先后在无源激光测距、可调谐半导体激光吸收 光谱TDLAS、智慧海绵城市监测评价物联网系统开发等技术上有重大研究成果 ，拥有3项发明专利，50项实用新型专利，24项外观专利，36项软件著作权。2014年公司被认定为“高新技术企业”。2015年10月公司完成股份制改造。 2015年12月通过ISO9001-2008质量管理体系认证。2016年7月先后取得信息系统集成资质证书、软企企业证书。2016年被成功认定为“瞪羚企业”。 目前公司面向消费者提供的产品包括物联网领域的软、硬件产品、光机电一体化传感器、火灾探测器、气体传感器、水利水文仪器仪表和设备 、环境监测治理仪器仪表和设备、气象监测仪器仪表的科研、开发、生产、销售、安装及售后服务。
                        </div>
                        <img src="~/assets/img/about/公司图片.png" alt="">
                    </div>
                </div>

            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                <TitleMsgShow title="研发实力" titleEN="COMPANY POWER"></TitleMsgShow>
                <div class="about-conent">
                    <div class="about-company">
                        <img src="~/assets/img/about/研发实力.png" alt="">
                        <div class="companyPower">
                            2012年诞生于有世界光谷之称的武汉东湖高新技术开发区， 公司位于武汉市东湖新技术开发区光谷大道303号光谷芯中心三期3-11幢1-5层1厂房单元， 面积1500平米。公司注册资本1000万元，实收资本1000万元。自创始以来，公司始终坚持走自主创新之路， 先后在无源激光测距、可调谐半导体激光吸收 光谱TDLAS、智慧海绵城市监测评价物联网系统开发等技术上有重大研究成果 ，拥有3项发明专利，50项实用新型专利，24项外观专利，36项软件著作权。2014年公司被认定为“高新技术企业”。2015年10月公司完成股份制改造。 2015年12月通过ISO9001-2008质量管理体系认证。2016年7月先后取得信息系统集成资质证书、软企企业证书。2016年被成功认定为“瞪羚企业”。 目前公司面向消费者提供的产品包括物联网领域的软、硬件产品、光机电一体化传感器、火灾探测器、气体传感器、水利水文仪器仪表和设备 、环境监测治理仪器仪表和设备、气象监测仪器仪表的科研、开发、生产、销售、安装及售后服务。
                        </div>
                    </div>
                    <div class="power-foot">
                        <Power num="6" titleEN="6年的经验" years="true"></Power>
                        <Power num="47" titleEN="47项实用新型专利"></Power>
                        <Power num="30" titleEN="30项外观专利"></Power>
                        <Power num="48" titleEN="48项软件著作权"></Power>

                    </div>
                </div>

            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                <TitleMsgShow title="企业理念" titleEN="solution"></TitleMsgShow>
                asdf
            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                <TitleMsgShow title="营销网络" titleEN="solution"></TitleMsgShow>
            </el-col>
        </el-row>
    </div>
</template>
<script>
import TitleMsgShow from "~/components/common/TitleMsgShow";
import Power from "~/components/about/Power";
export default {
  components: {
    TitleMsgShow,
    Power
  },
  data() {
    return {
      activeName: "second"
    };
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  }
};
</script>

<style scoped>
.aboutMain {
  margin-top: 101px;
}
.about-head {
  width: 100%;
  height: 300px;
  background-image: url("~/assets/img/about/关于我们.png");
  background-size: 100% 300px;
}
.about-conent {
  display: flex;
  width: 1400px;
  flex-direction: column;
  margin: 0 auto;
}
.about-company {
  display: flex;
}
.companyInfo {
  font-size: 14px;
  color: #333333;
  letter-spacing: 2px;
  line-height: 27px;
  padding-right: 60px;
}
.about-company > img {
  width: 560px;
  height: 470px;
}
.companyPower {
  font-size: 14px;
  color: #333333;
  letter-spacing: 2px;
  line-height: 27px;
  padding-left: 50px;
}
.power-foot {
  display: flex;
  justify-content: center;
}
.power-foot > div {
  width: 350px;
  height: 200px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>

