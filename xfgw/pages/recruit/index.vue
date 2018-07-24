<template>
    <div class="recruit-mian">
        <div class="recruit-head">
            <TitleMsgShow title="人才招聘" titleEN="TALENT RECRUITMENT" titleBackground="~/assets/img/linkme/人才招聘.png"></TitleMsgShow>
        </div>
        <el-row>
            <el-col :span="24" class="talent-conent">
                <TitleMsgShow title="人才理念" titleEN="TALENT CONCEPT"></TitleMsgShow>
                <div class="talent">
                    <p>德才兼备，以德为先，人才是公司最核心的竞争力！</p>
                </div>
            </el-col>
        </el-row>
        <el-row>
            <el-col :span="24">
                <TitleMsgShow title="招聘岗位" titleEN="RECRUITING POSITION"></TitleMsgShow>
                <div class="recruit-info">
                    <span>
                        欢迎广大业内精英加入我司，携手共创辉煌！以下我司最新招聘职位，如无合适职位，您亦可将简历发至如下邮箱: newfirber_hr@136.com,一旦有合适职位，我们会尽快和您取得联系。
                    </span>
                    <div class="table-info">
                        <el-table :data="newusers" stripe element-loading-text="给我一点时间" style="width: 100%">
                            <el-table-column align="center" width="230" label="职位名称">
                                <template slot-scope="scope">
                                    <span>{{scope.row.id}}</span>
                                </template>
                            </el-table-column>
                            <el-table-column width="230" align="center" label="招聘人数">
                                <template slot-scope="scope">
                                    <span>{{scope.row.userName}}</span>
                                </template>
                            </el-table-column>
                            <el-table-column min-width="230" width="230" align="center" label="招聘部门">
                                <template slot-scope="scope">
                                    <span>{{scope.row.password}}</span>
                                </template>
                            </el-table-column>
                            <el-table-column width="230" align="center" label="学历要求">
                                <template slot-scope="scope">
                                    <span>{{scope.row.age}}</span>
                                </template>
                            </el-table-column>
                            <el-table-column width="250" align="center" label="发布日期">
                                <template slot-scope="scope">
                                    <span v-if="scope.row.lnglat.length>0 && scope.row.lnglat[0].address !=''">{{scope.row.lnglat[0].address}}</span>
                                    <span v-else>该用户还未添加地址</span>
                                </template>
                            </el-table-column>
                            <el-table-column align="center" width="230">
                                <template slot-scope="scope">
                                    <span>详情</span>
                                </template>
                            </el-table-column>
                        </el-table>
                    </div>

                    <div class="pagination-container">
                        <el-pagination background @size-change="handleSizeChange" @current-change="handleCurrentChange" :current-page="listQuery.page" :page-sizes="[5,10,15, 20]" :page-size="listQuery.limit" layout="total, sizes, prev, pager, next, jumper" :total="total">
                        </el-pagination>
                    </div>
                </div>

            </el-col>
        </el-row>
    </div>
</template>

<script>
import axios from "axios";
import TitleMsgShow from "~/components/common/TitleMsgShow";
export default {
  components: {
    TitleMsgShow
  },
  data() {
    return {
      listQuery: {
        page: 1,
        limit: 5,
        userName: ""
      },
      total: null,
      newusers: []
    };
  },
  created() {
    this.getUsers();
  },
  methods: {
    //获取数据
    getUsers() {
      axios
        .get("http://39.108.100.163:8888/selectUserList", {
          params: {
            page: this.listQuery.page,
            rows: this.listQuery.limit,
            userName: this.listQuery.userName
          }
        })
        .then(response => {
          //consoleconsole.log(response);
          this.newusers = response.data.list;
          this.total = response.data.total;
        })
        .catch(error => {
          console.log("axios==" + error);
        });
    },
    //添加用户名的模糊搜索
    handleFilter() {
      this.listQuery.page = 1;
      this.getUsers();
    },
    //修改每页的数量，重新获取数据
    handleSizeChange(val) {
      this.listQuery.limit = val;
      this.getUsers();
    },
    // 修改第几页。
    handleCurrentChange(val) {
      this.listQuery.page = val;
      this.getUsers();
    }
  }
};
</script>

<style scoped>
.recruit-mian {
  margin-top: 101px;
}
.recruit-head {
  width: 100%;
  height: 300px;
  background-image: url("~/assets/img/recruit/人才招聘.png");
  background-size: 100% 300px;
}
.talent-conent {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 350px;
}
.talent {
  width: 1400px;
  height: 150px;
  display: flex;
  justify-content: center;
  background-image: url("~/assets/img/recruit/人才理念.png");
  background-size: 100% 150px;
}
.talent > p {
  display: flex;
  color: white;
  align-items: center;
  font-size: 20px;
}
.recruit-info {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.recruit-info > span {
  font-size: 14px;
  color: #333333;
  margin-bottom: 15px;
}
.table-info {
  width: 1400px;
}
.pagination-container {
  display: flex;
  height: 100px;
  align-items: center;
}
</style>
