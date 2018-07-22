<template>
    <div>
        <el-row type="flex" class="row-bg">
            <el-col :span="24">
                <div class="grid-content bg-purple-dark">联系我们</div>
            </el-col>
        </el-row>
        <el-row type="flex" class="row-bg" justify="center">
            <el-col :span="8">
                <div class="grid-content bg-purple">1</div>
            </el-col>
            <el-col :span="8">
                <div class="grid-content bg-purple-light">2</div>
            </el-col>
            <el-col :span="8">
                <div class="grid-content bg-purple">3</div>
            </el-col>
        </el-row>
        <el-row>
            <el-col>
                <div id="map">
                </div>
            </el-col>
        </el-row>
    </div>

</template>

<script>
import L from "leaflet/dist/leaflet.js";
import "leaflet/dist/leaflet.css";
export default {
  data() {
    return {};
  }
};
</script>

<style scoped>
#map {
  background: burlywood;
  height: 50vh;
}
</style>
