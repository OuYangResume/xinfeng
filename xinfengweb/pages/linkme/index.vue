<template>
    <div class="main">
        <div class="head">

        </div>
        <el-row type="flex" class="row-bg">
            <el-col :span="24">
                <div class="link-head">
                    <p>联系我们</p>
                    快速联系我们及时沟通，获得更多解决方案
                </div>
            </el-col>
        </el-row>
        <el-row type="flex" class="row-bg" justify="center">
            <el-col :span="8">
                <div class="link-content">
                    <p>业务电话:027-51895830</p>
                    <p>前台电话:027-50851666</p>
                    <p>人事电话:027-50851666</p>
                </div>
            </el-col>
            <el-col :span="8">
                <div class="link-content ">
                    <p>创新基地:武汉东湖高新区光谷大道</p>
                    <p>303光谷.芯中心C3-11栋</p>
                </div>
            </el-col>
            <el-col :span="8">
                <div class="link-content ">
                    <p>公司传真:027-59307758</p>
                    <p>联系邮箱:info@newfiber.com.cn</p>
                </div>
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
import Leaflet from "leaflet";
import("leaflet/dist/leaflet.css");
import mapProvider from "~/assets/js/leaflet.MapProviders.js";
export default {
  data() {
    return {
      map: null,
      map_config: {
        zoom: 17,
        center: [30.477117, 114.403471],
        minZoom: 3,
        maxZoom: 18
      }
    };
  },
  methods: {
    initMap: function() {
      this.map = L.map("map", {
        center: this.map_config.center,
        zoom: this.map_config.zoom,
        minZoom: this.map_config.minZoom,
        maxZoom: this.map_config.maxZoom,
        attribution: "&copy; 高德地图",
        zoomControl: false,
        logo: false
      });
      L.tileLayer
        .mapProvider("GaoDe.Normal.Map", {
          attribution: this.map_config.attribution
        })
        .addTo(this.map);
      L.marker([30.477117, 114.403471]).addTo(this.map);
    },
    addMapLayers() {}
  },
  mounted() {
    this.initMap();
  }
};
</script>

<style scoped>
.main {
  margin-top: 101px;
}
.head {
  width: 100%;
  height: 300px;
  background-color: aqua;
  background-image: url("~/assets/img/linkme/联系我们.png");
}
.link-head {
  height: 200px;
  width: 100%;
  text-align: center;
}
.link-head > p {
  font-size: 35px;
  margin-bottom: 20px;
  padding-top: 30px;
}
.link-content {
  height: 300px;
  width: 100%;
  text-align: center;
}
#map {
  height: 500px;
}
</style>
