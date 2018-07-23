<template>
  <el-container>
    <el-header>
      <Header></Header>
    </el-header>
    <el-main>
      <nuxt keep-alive />
    </el-main>
    <el-footer>
      <Footer></Footer>
    </el-footer>
  </el-container>
</template>
<script>
import Header from '../components/Header'
import Footer from '../components/Footer'

export default {
  data() {
    return {
      activeIndex: "/"
    };
  },
  created() {
    this.activeIndex = this.$route.path;
  },
  components: {
    Header,
    Footer
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
.el-main{
  padding: 0;
  background: rgba(241,241,241,1);
}
.el-footer {
  padding: 0;
}
</style>

