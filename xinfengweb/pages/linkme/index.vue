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
        <!-- <el-row>
            <el-col>
                <div id="map">
                </div>
            </el-col>
        </el-row> -->
        <div id="map"></div>
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
        zoom: 10,
        center: [37.5, 106],
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
        // scrollWheelZoom: false,
        logo: false
      });
      L.tileLayer
        .mapProvider("GaoDe.Normal.Map", {
          attribution: this.map_config.attribution
        })
        .addTo(this.map);
    },
    addMapLayers() {}
  },
  mounted() {
    this.initMap();
  }
};
</script>

<style scoped>
#map {
  height: 50vh;
  margin-left: -20px;
  margin-right: -20px;
}
</style>
