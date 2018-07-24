<template>
  <div class="iviewTabBox">
    <Tabs value="name1">
        <TabPane label="公司新闻" name="name1">
          <div class="tabContent">
              <li v-for="(item, index) in companyNewsList" :key="index">
                <AllMsgList :time="item.createTime" :title="item.title" :digest="item.digest" :contentId="item.contentId"></AllMsgList>
              </li>
          </div>
        </TabPane>
        <TabPane label="行业资讯" name="name2">
          <div>
              <li v-for="(item, index) in industryInformation" :key="index">
                <AllMsgList :time="item.createTime" :title="item.title" :digest="item.digest" :contentId="item.contentId"></AllMsgList>
              </li>
          </div>
        </TabPane>
        <TabPane label="展会信息" name="name3">
          <div>
              <li v-for="(item, index) in exhibitionInformation" :key="index">
                <AllMsgList :time="item.createTime" :title="item.title" :digest="item.digest" :contentId="item.contentId"></AllMsgList>
              </li>
          </div>
        </TabPane>
    </Tabs>
  </div>
</template>
<script>
import AllMsgList from "./AllMsgList";

export default {
  props: {
    companyNewsList: {
      type: Array
    },
    industryInformation: {
      type: Array
    },
    exhibitionInformation: {
      type: Array
    },
  },
  components: {
    AllMsgList
  }
};
</script>
<style>
.iviewTabBox .ivu-tabs-nav .ivu-tabs-tab {
    font-size: 16px !important;
}
</style>
