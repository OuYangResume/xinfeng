<template>
    <div>
      <el-menu :default-active="nowActive" class="el-menu-vertical-demo" @select="handleSelect" :collapse="isCollapse">
        <el-submenu index="1">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span slot="title">气联网产品</span>
          </template>
          <el-menu-item-group>
            <!-- <span slot="title">分组一</span> -->
            <el-menu-item index="g1">时差式流量计</el-menu-item>
            <el-menu-item index="g2">气泡水位计</el-menu-item>
            <el-menu-item index="g3">多普勒超声波流速仪</el-menu-item>
            <el-menu-item index="g4">一体化水文站</el-menu-item>
            <el-menu-item index="g5">水位计控制器</el-menu-item>
            <el-menu-item index="g6">浊度计</el-menu-item>
            <el-menu-item index="g7">容栅式雨量计</el-menu-item>
            <el-menu-item index="g8">闸位计</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
        <el-submenu index="2">
          <template slot="title">
            <!-- <i class="el-icon-location"></i> -->
            <span slot="title">气联网产品</span>
          </template>
          <el-menu-item-group>
            <!-- <span slot="title">分组一</span> -->
            <el-menu-item index="g9">激光瓦斯检测仪</el-menu-item>
            <el-menu-item index="g10">光纤液位计</el-menu-item>
          </el-menu-item-group>
        </el-submenu>
      </el-menu>
    </div>
</template>

<script>
export default {
  data() {
    return {
      isCollapse: false,
      defaultIndex: 'g1',
      // defaultOpeneds: [1, 2]
    };
  },
  props: {
    nowActive: {
      type: String
    }
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    },
    handleSelect(index, keyPath) {
      console.log(index, keyPath)
      this.$router.push(`/production/${index}`)
    }
  },
  mounted() {
    
  },
};
</script>

<style>
.el-menu-vertical-demo:not(.el-menu--collapse) {
  width: 200px;
  min-height: 400px;
}
</style>
