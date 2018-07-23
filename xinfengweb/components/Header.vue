<template>
    <el-menu :default-active="activeIndex" mode="horizontal" router>
        <el-menu-item index="/">网站首页</el-menu-item>
        <el-menu-item index="/news">新闻动态</el-menu-item>
        <el-menu-item index="/tab/tech">产品中心</el-menu-item>
        <el-menu-item index="/tab/solution">解决方案</el-menu-item>
        <el-menu-item index="/tab/play">成功案例</el-menu-item>
        <el-menu-item index="/tab/apple">营销服务</el-menu-item>
        <el-menu-item index="/tab/play1">人才招聘</el-menu-item>
        <el-menu-item index="/about/inasdf">关于我们</el-menu-item>
        <el-menu-item index="/linkme">联系我们</el-menu-item>
    </el-menu> 
</template>
<script>
export default {
    
}
</script>
<style scoped>
.el-menu--horizontal>.el-menu-item {
    float: left;
    height: 100px !important;
    line-height: 100px !important;
    padding: 0 20px;
    font-size: 16px;
    font-weight: bold;
    color: #333;
}
.el-menu--horizontal>.el-menu-item.is-active {
    border-bottom: 2px solid #409EFF;
    color: #005966;
}
.el-menu--horizontal {
    width: 100%;
    display: flex;
    justify-content: center;
}
</style>
