<template>
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
</template>
<script>
export default {};
</script>
<style scoped>
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
