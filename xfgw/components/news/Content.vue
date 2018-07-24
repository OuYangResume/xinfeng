<template>
  <el-tabs v-model="activeName" @tab-click="handleClick">
    <el-tab-pane label="公司新闻" name="first">
        
    </el-tab-pane>
    <el-tab-pane label="行业资讯" name="second">配置管理</el-tab-pane>
    <el-tab-pane label="展会信息" name="third">角色管理</el-tab-pane>
  </el-tabs>
</template>
<script>
  export default {
    data() {
      return {
        activeName: 'second'
      };
    },
    methods: {
      handleClick(tab, event) {
        console.log(tab, event);
      }
    }
  };
</script>