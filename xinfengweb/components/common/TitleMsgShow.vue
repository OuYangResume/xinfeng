<template>
    <div v-if="titleBackground" class="solution-title" v-bind:style="{background: 'url(' + titleBackground + ')'}">
        <div class="solution-text">{{title}}</div>
        <div class="solution-hr"></div>
        <div class="solution-describle solution-describle-bg">
          <span>{{titleEN}}</span>
        </div>
    </div>
    <div v-else class="solution-title" v-bind:style="{background: 'url(' + titleBackground + ')'}">
        <div class="solution-text">{{title}}</div>
        <div class="solution-describle">
          <hr>
          <span>{{titleEN}}</span>
          <hr>
        </div>
    </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    titleEN: {
      type: String,
      required: true
    },
    titleBackground: {
      type: String,
    }
  },
};
</script>
<style scoped>
.solution-title {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 30px 0;
}
.solution-hr{
  margin: 5px 0;
  width: 35px;
  height: 2px;
  background: white;
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
  min-width: 100px;
  text-align: center;
}
.solution-describle-bg > span{
  font-size: 16px;
}
.solution-describle > hr {
  width: 50px;
}
</style>
