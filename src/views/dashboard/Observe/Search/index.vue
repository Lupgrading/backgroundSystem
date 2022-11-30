<template>
  <el-card class="box-card">
    <div slot="header" class="header">
      <div class="search-header">
        <span>线上热门搜索</span>
        <el-dropdown>
          <span class="el-dropdown-link">
            <i class="el-icon-more"></i>
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>黄金糕</el-dropdown-item>
            <el-dropdown-item>狮子头</el-dropdown-item>
            <el-dropdown-item>螺蛳粉</el-dropdown-item>
            <el-dropdown-item>双皮奶</el-dropdown-item>
            <el-dropdown-item>蚵仔煎</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
    </div>
    <div>
      <el-row :gutter="10">
        <el-col :span="12"><LineCharts></LineCharts></el-col>
        <el-col :span="12"><LineCharts></LineCharts></el-col>
      </el-row>
    </div>
    <!-- table表格 -->
    <template>
      <el-table style="width: 100%" border>
        <el-table-column type="index" label="排名" width="80">
        </el-table-column>
        <el-table-column prop="prop" label="搜索关键字" width="180">
        </el-table-column>
        <el-table-column prop="prop" label="用户数" sortable> </el-table-column>
        <el-table-column prop="prop" label="周涨幅" sortable> </el-table-column>
      </el-table>
    </template>
    <!-- 分页器 -->
    <el-pagination layout="prev, pager, next" :total="1000" class="pagination">
    </el-pagination>
  </el-card>
</template>

<script>
import LineCharts from "./lineCharts";
export default {
  name: "",
  components: {
    LineCharts,
  },
};
</script>

<style scoped>
.header {
  border-bottom: 1px solid #e4e7ed;
  padding: 5px 0;
}
.search-header {
  display: flex;
  justify-content: space-between;
}
.pagination {
  float: right;
}
</style>
