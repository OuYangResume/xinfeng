<template>
    <div class="power-main">
        <div class="power-num">
            <div class="power-count">{{num}}</div>
            <p v-if="years" class="power-marker1">YEARS</p>
            <p v-else class="power-marker2">+</p>
        </div>
        <div class="power-text">{{titleEN}}</div>
    </div>
</template>
<script>
export default {
  props: {
    num: {
      type: String,
      required: true
    },
    titleEN: {
      type: String,
      required: true
    },
    years: {
      type: String
    }
  }
};
</script>

<style scoped>
.power-mian {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 200px;
}
.power-num {
  display: flex;
  color: #076ce0;
}
.power-count {
  font-size: 50px;
}
.power-marker1 {
  font-size: 20px;
  margin-top: 31px;
  margin-left: 10px;
}
.power-marker2 {
  font-size: 35px;
  margin-left: 5px;
}
.power-text {
  font-size: 16px;
  color: #999999;
}
</style>
