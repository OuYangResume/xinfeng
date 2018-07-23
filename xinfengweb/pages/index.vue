<template>
  <div>
    <div class="lunbo">
      <div class="block">
        <el-carousel trigger="click" height="640px">
          <el-carousel-item v-for="item in imgList" :key="item">
            <h3>
              <img :src="item" alt="">
            </h3>
          </el-carousel-item>
        </el-carousel>
      </div>
    </div>
    <Classical></Classical>
    <div class="main-solution">
      <!-- <TitleMsgShow title="解决方案" titleEN="solution" titleBackground="https://i.loli.net/2018/07/22/5b545633ca9c9.png"></TitleMsgShow> -->
      <TitleMsgShow title="解决方案" titleEN="solution"></TitleMsgShow>
      <div class="solutionType">
        <div class="ssc-solution">
          <div class="solutionImgBox">
            <img src="~assets/img/solutionImg1.png" alt="智慧海绵城市">
          </div>
          <div>智慧海绵城市</div>
        </div>
        <div class="smartWater">
          <div class="solutionImgBox">
            <img src="~assets/img/solutionImg2.png" alt="智慧水文">
          </div>
          <div>智慧水文</div>
        </div>
        <div class="smartDewatering">
          <div class="solutionImgBox">
            <img src="~assets/img/solutionImg3.png" alt="智慧排水">
          </div>
          <div>智慧排水</div>
        </div>
        <div class="governWater">
          <div class="solutionImgBox">
            <img src="~assets/img/solutionImg4.png" alt="黑臭水体治理">
          </div>
          <div>黑臭水体治理</div>
        </div>
        <div class="smartWaterPerson">
          <div class="solutionImgBox">
            <img src="~assets/img/solutionImg5.png" alt="智慧河长">
          </div>
          <div class="">智慧河长</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Classical from '../components/Classical'
import TitleMsgShow from '../components/common/TitleMsgShow'
export default {
  data () {
    return {
      imgList:     
        [
          'http://www.newfiber.com.cn/d/file/content/2016/10/581166208bb6a.jpg',
          'http://www.newfiber.com.cn/d/file/content/2017/03/58c73fedd9c0d.jpg',
          'http://www.newfiber.com.cn/d/file/content/2017/03/58c6757a9f44e.jpg'
        ]
    }
  },
  // props: {
  //   imgList: {
  //     type: Array,
  //     required: true
  //   }
  // },
  components: {
    Classical,
    TitleMsgShow
  }
};
</script>
<style scoped>
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
.solutionType {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-bottom: 80px;
}
.solutionType > div {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  margin: 0 3vw;
}
.solutionType > div > div:nth-child(2) {
  font-size: 18px;
  font-weight: bold;
}
</style>






