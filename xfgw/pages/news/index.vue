<template>
    <div>
        <div class="head">
            <TitleMsgShow title="新闻动态" titleEN="NEWS CENTER" titleBackground="123"></TitleMsgShow>
        </div>
        <div class="contentBigBox">
            <div class="contentBox">
                <!-- <Content></Content> -->
                <ManyNewsShow :companyNewsList="companyNewsList" :industryInformation="industryInformation" :exhibitionInformation="exhibitionInformation"></ManyNewsShow>
            </div>
        </div>
    </div>

</template>
<script>
import axios from "axios";
import TitleMsgShow from "../../components/common/TitleMsgShow.vue";
import Content from "../../components/news/Content.vue";
import ManyNewsShow from "../../components/news/ManyNewsShow.vue";

export default {
  data() {
    return {
      companyNewsList: null,
      industryInformation: null,
      exhibitionInformation: null,
      imgUrl: "~/assets/img/recruit/rencai.png"
    };
  },
  components: {
    TitleMsgShow,
    Content,
    ManyNewsShow
  },
  mounted() {
    axios
      .get("http://192.168.30.208:9000/XFGD/goPage?pageId=002")
      .then(response => {
        this.companyNewsList = JSON.parse(response.data.b);
        this.industryInformation = JSON.parse(response.data.c);
        this.exhibitionInformation = JSON.parse(response.data.d);
      })
      .catch(function(error) {
        // handle error
        console.log(error);
      })
      .then(function() {
        // always executed
      });
  }
};
</script>
<style scoped>
.head {
  width: 100%;
  height: 300px;
  background-color: aqua;
  background-image: url("~/assets/img/linkme/联系我们.png");
  background-size: 100% 300px;
  margin-top: 100px;
}
.contentBigBox {
  display: flex;
  justify-content: center;
}
.contentBox {
  margin-top: 20px;
  width: 1250px;
}
</style>


