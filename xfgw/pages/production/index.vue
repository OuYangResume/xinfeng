<template>
    <div>
        <div class="head">
            <TitleMsgShow title="产品中心" titleEN="PRODUCT CENTER" titleBackground="123"></TitleMsgShow>
        </div>
        <div class="contentBigBox">
            <div class="contentBox">
                <div class="iviewTabBox">
                    <Tabs value="name1">
                        <TabPane label="水联网产品" name="name1">
                        <div class="tabContent">
                            <ProductShowList :nowActive="nowActive"></ProductShowList>
                            <div class="listImgBox">
                                <li v-for="(item, index) in contentSimple" :key="index">
                                    <!-- <div>{{item}}</div> -->
                                    <ProductShow :imgSrc="item.titleImage" :imgTitle="item.title"></ProductShow>
                                </li>
                            </div>
                        </div>
                        </TabPane>
                        <TabPane label="气联网系列" name="name2">
                        <div>
                            <!-- <li v-for="(item, index) in allAirProduct" :key="index">
                                <ProductShow :imgSrc="itme.imgSrc" :imgTitle="item.title"></ProductShow>
                            </li> -->
                        </div>
                        </TabPane>
                    </Tabs>
                </div>
            </div>
        </div>
    </div>

</template>
<script>
import axios from "axios";
import TitleMsgShow from "../../components/common/TitleMsgShow"
import ProductShow from '../../components/production/ProductShow'
import ProductShowList from '../../components/production/ProductShowList'

export default {
  data() {
    return {
      allWaterProduct: null,
      allAirProduct: null,
      contentSimple: null,
      nowActive: 'g1'
    };
  },
  components: {
    ProductShow,
    TitleMsgShow,
    ProductShowList
  },
//   async asyncData({ params, error }) {
//     const contents = await axios.get("http://192.168.30.208:9000/XFGD/goPage?pageId=003");
//     console.log(contents)
//     const contentSimple = JSON.parse(contents.data);
//     return {
//       contents,
//       contentSimple
//     };
//   },
  mounted() {
    axios
      .get("http://192.168.30.208:9000/XFGD/goPage?pageId=003")
      .then(response => {
          console.log(response.data.g1)
          contentSimple = response.data.g1
        // this.allWaterProduct = JSON.parse(response.data.b);
        // this.allAirProduct = JSON.parse(response.data.c);
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
  padding-bottom: 50px;
}
.tabContent {
  display: flex;
}
.contentBox {
  margin-top: 20px;
  width: 1250px;
}
.listImgBox {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start;
}
.el-menu-vertical-demo {
  border: none !important;
}
</style>


