<template>
<div>
  <section>
    <!-- 工具条 -->
    <el-col :span="24" class="toolbar" style="padding-bottom: 0px;">
      <el-form :inline="true" :model="filters">
        <el-form-item>
          <el-input v-model="filters.name" placeholder="姓名"></el-input>
        </el-form-item>
        <el-form-item>
          <el-button  type="primary" icon="el-icon-search"  @click="getUsers">查询</el-button>
        </el-form-item>
        <el-form-item>
          <el-button type="primary" icon="el-icon-plus"  @click="handleAdd">新增</el-button>
        </el-form-item>
      </el-form>
    </el-col>
    <!-- 列表 -->
    <el-table :data="users" highlight-current-row v-loading="listLoading" @selection-change="selsChange" style="100%">
      <el-table-column type="selection" width="55"></el-table-column>
      <el-table-column type="index" width="60"></el-table-column>
      <el-table-column prop="name" label="姓名" width="120" sortable></el-table-column>
      <el-table-column prop="sex" label="性别" width="100" :formatter="formatSex" sortable></el-table-column>

    </el-table>
  </section>
</div>
</template>

<script>
export default {
  data () {
    return {
      filters: {
        name: ''
      }
    };
  },

  methods: {
    // 性别显示转换
    formatSex: function (row, column) {
      return row.sex === 1 ? '男' : row.sex === 0 ? '女' : '未知';
    },
    // 获取用户列表
    getUsers () {

    },
    // 显示新增界面
    handleAdd () {

    }
  }
};
</script>

<style scoped>

</style>
