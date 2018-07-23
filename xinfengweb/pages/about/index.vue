<template>
    <div class="aboutMain">
        <el-row>
            <el-col :span="12">
                <div>
                    <el-tabs v-model="activeName" @tab-click="handleClick">
                        <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
                        <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
                        <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
                        <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
                    </el-tabs>
                </div>
            </el-col>
            <el-col :span="12">
                <div>
                    <el-breadcrumb separator-class="el-icon-arrow-right">
                        <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
                        <el-breadcrumb-item>活动管理</el-breadcrumb-item>
                        <el-breadcrumb-item>活动列表</el-breadcrumb-item>
                        <el-breadcrumb-item>活动详情</el-breadcrumb-item>
                    </el-breadcrumb>
                </div>
            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                <TitleMsgShow title="解决方案" titleEN="solution"></TitleMsgShow>
                公司介绍
            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                研发实力
            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                企业理念
            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                营销网络
            </el-col>
        </el-row>
    </div>
</template>
<script>
import TitleMsgShow from "~/components/common/TitleMsgShow";
export default {
  components: {
    TitleMsgShow
  },
  data() {
    return {
      activeName: "second"
    };
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  }
};
</script>

<style scoped>
.aboutMain {
  margin-top: 101px;
}
</style>

