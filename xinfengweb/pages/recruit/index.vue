<template>
    <div class="recruit-mian">
        <el-row>
            <el-col :span="24">
                <TitleMsgShow title="人才理念" titleEN="TALENT CONCEPT"></TitleMsgShow>
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
                        <el-table :data="newusers" element-loading-text="给我一点时间" show-header highlight-current-row:true style="width: 100%">

                            <el-table-column align="center" width="150" label="职位名称">
                                <template slot-scope="scope">
                                    <span>{{scope.row.id}}</span>
                                </template>
                            </el-table-column>
                            <el-table-column width="150px" align="center" label="招聘人数">
                                <template slot-scope="scope">
                                    <span>{{scope.row.userName}}</span>
                                </template>
                            </el-table-column>
                            <el-table-column min-width="150px" width="80" align="center" label="招聘部门">
                                <template slot-scope="scope">
                                    <span>{{scope.row.password}}</span>
                                </template>
                            </el-table-column>
                            <el-table-column width="110px" align="center" label="学历要求">
                                <template slot-scope="scope">
                                    <span>{{scope.row.age}}</span>
                                </template>
                            </el-table-column>
                            <el-table-column width="180" align="center" label="发布日期">
                                <template slot-scope="scope">
                                    <span v-if="scope.row.lnglat.length>0 && scope.row.lnglat[0].address !=''">{{scope.row.lnglat[0].address}}</span>
                                    <span v-else>该用户还未添加地址</span>
                                </template>
                            </el-table-column>
                            <el-table-column align="center" width="65">
                                <template slot-scope="scope">
                                    <span>详情</span>
                                </template>
                            </el-table-column>
                        </el-table>
                    </div>

                    <div class="pagination-container">
                        <el-pagination background @size-change="handleSizeChange" @current-change="handleCurrentChange" :current-page="listQuery.page" :page-sizes="[3,5,8, 10]" :page-size="listQuery.limit" layout="total, sizes, prev, pager, next, jumper" :total="total">
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
        limit: 3,
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
.recruit-info {
  display: flex;
  flex-direction: column;
}
.recruit-info > span {
  font-size: 14px;
  color: #333333;
  display: flex;
  justify-content: center;
}
.pagination-container {
  display: flex;
  justify-content: center;
}
</style>
