<template>
    <div>
        <Tabs value="tab1">
            <TabPane label="网站首页" name="tab1"></TabPane>
            <TabPane label="新闻动态" name="tab2"></TabPane>
            <TabPane label="产品中心" name="tab3"></TabPane>
            <TabPane label="解决方案" name="tab4"></TabPane>
            <TabPane label="成功案例" name="tab5"></TabPane>
            <TabPane label="营销服务" name="tab6"></TabPane>
            <TabPane label="人才招聘" name="tab7"></TabPane>
            <TabPane label="关于我们" name="tab8"></TabPane>
            <TabPane label="联系我们" name="tab9"></TabPane>
        </Tabs>
    </div>
</template>
<script>
    export default {
        
    }
</script>
<style>
.ivu-tabs-bar{
    margin-bottom: 0px;
}
.ivu-tabs-nav .ivu-tabs-tab {
    padding: 38px 16px;
    font-size: 16px;
    color: #333;
    font-weight: bolder;
}
.ivu-tabs-nav .ivu-tabs-tab-active {
    color: #005699;
}
.ivu-tabs-nav-scroll {
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
