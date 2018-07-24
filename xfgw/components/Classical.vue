<template>
    <div class="content_10_18" style="width:1200px; margin:50px auto; min-height: 100px; overflow: hidden; padding-bottom: 0px; ">
      <!-- <div class="jdal">
        <h2 style="font-size: 16px;padding-bottom:10px; color: #000509;">经典案例</h2>
      </div> -->
        <ul class="nav">
          <li v-for="(item, index) of classicalExample" :key="index">
            <div class="li_img"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=91">
            <img :src="item.titleImage" width="300" height="200"></a>
            </div>
            <div class="box">
                <a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=91">
                <div class="ckxq" style="display: none;"><span>查看详情</span></div>
                <div class="jt" style="display: none;"></div>
                <h1>{{ item.title}}</h1>
                <p class="hiddenRows">{{ item.digest}}</p>
                <!-- <p> 镇江作为全国首批入围海绵城市试点城市，早在2007年就在生态排水、城市低影响开发方面有所研究，着手开展城市雨型及降雨量、径流量控制、面源污染控制、初期雨水截流等相关研究工作，并在近年的城市建设中将“智慧海绵城市SSC”的理念渗透在具体建设细节中，打造海绵城市一体化建设。镇江市示范区海绵城市建设主要目标为......</p> -->
              </a>
            </div>
          </li>
          <!-- <li>
            <div class="li_img"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=91">
            <img :src="classicalExample2.titleImage" width="300" height="200"></a>
            </div>
            <div class="box">
                <a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=91">
                <div class="ckxq" style="display: none;"><span>查看详情</span></div>
                <div class="jt" style="display: none;"></div>
                <h1>{{ classicalExample2.title}}</h1>
                <p class="hiddenRows">{{ classicalExample2.digest}}</p>
              </a>
            </div>
          </li> -->
          <!-- <li>
            <div class="box">
              <a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=88">
              <div class="ckxq" style="display: none;">
                <span>查看详情</span>
                </div>
              <div class="jt" style="display: none;"></div>
              <h1>西宁市海绵城市建设</h1>
              <p>西宁市在全省生态建设中承担着引领和示范责任，建设海绵城市是生态文明先行先试的重要支撑。多年来，西宁市持续发力改善人居环境，重点实施了环城国家森林公园、火烧沟冲沟治理、北川河湿地公园、新华联小区等一批由大到小的海绵体建设，积累了多种类型以海绵理念进行生态修复的经验。为了在全市范围内推广海绵建设的理念，提高管理......</p>
            </a></div><div class="li_img"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=88"><img src="http://www.newfiber.com.cn/statics/default/images/56b46af91c702f59fecd5ae9a36b800e.jpg" width="300" height="200"></a></div>
          </li> -->
          <!-- <li><div class="li_img"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=86"><img src="http://www.newfiber.com.cn/statics/default/images/56b46af91c702f59fecd5ae9a36b800e.jpg" width="300" height="200"></a></div><div class="box"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=86">
              <div class="ckxq" style="display: none;"><span>查看详情</span></div>
              <div class="jt" style="display: none;"></div>
              <h1>武汉市海绵城市建设</h1>
              <p>根据武汉市海绵城市建设要求：年径流总量控制率达到78%，降雨控制厚度30mm；SS年控制率达到60%；雨水回用率不小于15%。项目充分考虑原有竖向，合理划分汇水分区，通过设置雨水中庭、雨水花园、生态停车场、植草沟、彩色透水混凝土、雨水调蓄池等LID措施消纳规划范围内雨水......</p>
            </a></div>
          </li> -->
          <!-- <li><div class="box"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=87">
              <div class="ckxq" style="display: none;"><span>查看详情</span></div>
              <div class="jt" style="display: none;"></div>
              <h1>{{classicalExample3.title}}</h1>
              <p>{{classicalExample3.digest}}</p>
            </a></div><div class="li_img"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=87">
            <img :src="classicalExample3.titleImage" width="300" height="200"></a></div>
          </li>
          <li><div class="box"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=88">
              <div class="ckxq" style="display: none;"><span>查看详情</span></div>
              <div class="jt" style="display: none;"></div>
              <h1>{{classicalExample4.title}}</h1>
              <p>{{classicalExample4.digest}}</p>
            </a></div><div class="li_img"><a href="http://www.newfiber.com.cn/index.php?a=shows&catid=60&id=88">
            <img :src="classicalExample4.titleImage" width="300" height="200"></a></div>
          </li> -->
        </ul>
    </div>
</template>
<script>
export default {
  data () {
    return {
      classicalExample1: null,
      classicalExample2: null,      
      classicalExample3: null,
      classicalExample4: null,
    }
  },
  props: {
    classicalExample: {
      type: Array
    }
  },
  methods: {
    sliceData() {
      classicalExample1 = classicalExample[0],
      classicalExample2 = classicalExample[1],
      classicalExample3 = classicalExample[2],
      classicalExample4 = classicalExample[3]
    }
  },
  mounted() {
    // sliceData()
  },
}
</script>
<style scoped>
.content_10_18 a {
  color: #000;
}
.content_10_18 .nav {
  width: 1220px;
}
.content_10_18 .nav li {
  width: 600px;
  /* display: inline; */
  float: left;
  height: 200px;
  overflow: hidden;
}
.content_10_18 .nav .li_img {
  width: 300px;
  height: 200px;
  float: left;
  overflow: hidden;
}
.content_10_18 .nav .box {
  background: #fff;
  width: 300px;
  height: 200px;
  float: left;
  position: relative;
  padding: 20px;
  overflow: hidden;
  border-bottom: 1px solid #ccc
}
.content_10_18 .nav .li_img img {
  width: 300px;
  height: 200px;
  -moz-transition: 1s;
  -webkit-transition: 1s;
  -o-transition: 1s;
  transition: 1s;
}
.content_10_18 .nav .li_img img:hover {
  opacity: 0.8;
  transform: scale(1.1);
  -webkit-transform: scale(1.1);
  -moz-transform: scale(1.1);
}
.content_10_18 .nav .jt {
  width: 300px;
  height: 200px;
  position: absolute;
  top: 0px;
  left: 0px;
  background: #fff;
  filter: alpha(opacity=80);
  -moz-opacity: 0.8;
  -khtml-opacity: 0.8;
  opacity: 0.8;
}
.content_10_18 .nav .ckxq {
  width: 300px;
  text-align: center;
  position: absolute;
  top: 90px;
  left: 0px;
  z-index: 999;
}
.content_10_18 .nav .ckxq span {
  padding: 10px;
  border: 1px solid #000;
}
.content_10_18 .nav p {
  color: #666666;
  font-size: 13px;
}
.content_10_18 .nav li h1 {
  font-size: 16px;
}
.hiddenRows {
  position: relative;
  line-height: 24px;
  /* 3 times the line-height to show 3 lines */
  height: 145px;
  overflow: hidden;
}
.hiddenRows::after {
  content: "...";
  font-weight: bold;
  position: absolute;
  bottom: 0;
  right: 0;
  padding: 0 20px 1px 45px;
  background: url(http://css88.b0.upaiyun.com/css88/2014/09/ellipsis_bg.png)
    repeat-y;
}
</style>
