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
                            <ProductShowList :nowActive="nowActive1"></ProductShowList>
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
import TitleMsgShow from "../../components/common/TitleMsgShow";
import ProductShow from "../../components/production/ProductShow";
import ProductShowList from "../../components/production/ProductShowList";

export default {
  data() {
    return {
      allWaterProduct: null,
      allAirProduct: null,
      nowActive: null
    };
  },
  components: {
    ProductShow,
    TitleMsgShow,
    ProductShowList
  },
  async asyncData({ params, error }) {
    console.log(1)
    const nowActive1 = params.production
    const contents = await axios.get(
      `http://192.168.30.208:9000/XFGD/goPage?pageId=003&type=${
        params.production
      }`
    );
    const contentSimple = contents.data;
    return {
      nowActive1,
      contents,
      contentSimple
    };
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


