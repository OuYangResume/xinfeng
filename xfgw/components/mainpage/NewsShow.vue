<template>
  <div class="iviewTabBox">
    <Tabs value="name1">
        <TabPane label="公司新闻" name="name1">
          <div class="tabContent">
              <li v-for="(item, index) in companyNewsList" :key="index">
                <MsgList :time="item.createTime" :title="item.title" :digest="item.digest" :contentId="item.contentId"></MsgList>
              </li>
          </div>
        </TabPane>
        <TabPane label="行业资讯" name="name2">
          <div>
              <li v-for="(item, index) in industryInformation" :key="index">
                <MsgList :time="item.createTime" :title="item.title" :digest="item.digest" :contentId="item.contentId"></MsgList>
              </li>
          </div>
        </TabPane>
        <TabPane label="展会信息" name="name3">
          <div>
              <li v-for="(item, index) in exhibitionInformation" :key="index">
                <MsgList :time="item.createTime" :title="item.title" :digest="item.digest" :contentId="item.contentId"></MsgList>
              </li>
          </div>
        </TabPane>
    </Tabs>
  </div>
</template>
<script>
import MsgList from "./MsgList";

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
    MsgList
  }
};
</script>
<style>
.iviewTabBox .ivu-tabs-bar {
    border: none !important;
}
.iviewTabBox .ivu-tabs-nav .ivu-tabs-tab:hover {
    color: white !important;
    background: #3380ff !important;
}
.iviewTabBox .ivu-tabs-nav .ivu-tabs-tab-active {
    color: white !important;
    background: #3380ff !important;
}
.iviewTabBox .ivu-tabs-nav .ivu-tabs-tab {
    font-size: 16px !important;
    background: #f0f0f0;
}
</style>
