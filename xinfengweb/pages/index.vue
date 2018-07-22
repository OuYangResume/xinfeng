<template>
  <div>
    <div class="lunbo">
    </div>
    <div class="main-solution">
      <div class="solution-title">
        <div class="solution-text">解决方案</div>
        <div class="solution-describle">
          <hr>
          <span>solution</span>
          <hr>
        </div>
      </div>
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
export default {
  components: {}
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
  margin-top: 99px;
  width: 100%;
  height: 640px;
  background: #005699;
}
.main-solution {
  height: 460px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
.solution-title {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 30px;
}
.solution-text {
  font-size: 26px;
  color: #005699;
}
.solution-describle {
  display: flex;
  justify-content: center;
  align-items: center;
}
.solution-describle > span {
  margin: 0 10px;
  font-size: 14px;
  color: #999;
}
.solution-describle > hr {
  width: 50px;
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






