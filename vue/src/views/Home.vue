<template>
  <div>
    <div class="card" style="margin-bottom: 5px">
      <el-input style="width: 260px;margin-right: 5px" v-model="data.name" placeholder="请输入名称查询":prefix-icon="Search"></el-input>
      <el-input style="width: 260px;margin-right: 5px" v-model="data.name" placeholder="请输入账号查询":prefix-icon="Search"></el-input>
      <el-button type="primary">查 询</el-button>
      <el-button type="primary">重 置</el-button>
    </div>
    <div class="card" style="margin-bottom: 5px">
      <el-button type="danger">添加账户</el-button>
      <el-button type="primary">编辑账户</el-button>
      <el-button type="success">删除账户</el-button>
      <el-button type="info">重置账户</el-button>
    </div>
    <div class="card" style="margin-bottom:5px">
      <
      <el-table :data="data.tableData"style="width: 100%" :header-cell-style="{fontWeight:'bold',color:'#333',backgroundColor:'#eaf4ff'}">
        <el-table-column prop="name" label="名称" width="180"/>
        <el-table-column prop="phone" label="电话" />
        <el-table-column prop="address" label="地址" width="180"/>
      </el-table>
    </div>
  <div class="card">
    <el-pagination>
        v-model:current-page="data.pageNum"
        :page-size="data.pageSize"
        layout="total, prev, pager, next"
        :total="data.total"

    </el-pagination>
    </div>
  </div>


<!--  <div class="mb-4">-->
<!--    <el-button>Default</el-button>-->
<!--    <el-button type="primary">Primary</el-button>-->
<!--    <el-button type="success">Success</el-button>-->
<!--    <el-button type="info" >Info</el-button>-->
<!--    <el-button type="warning">Warning</el-button>-->
<!--    <el-button type="danger">Danger</el-button>-->
<!--  <div style="padding: 50px">-->
<!--    <el-icon size="25" color="green"><ChatDotRound /></el-icon>-->
<!--    <el-input  placeholder="placeholder":suffix-icon="Calendar":prefix-icon="Search"> </el-input>-->
<!--    <el-button type="primary" icon="Search">按钮</el-button>-->
<!--  </div>-->
<!--  </div>-->
</template>

<script  setup>

import {Calendar, ChatDotRound, Search} from "@element-plus/icons-vue";
import{reactive} from "vue";

const data = reactive({
  name:null,
  pageNum:1,
  pageSize:5,
  total:6,
  tableData:[
    {name:'董明明', phone:'15241264822',address:'鞍山市铁东区'}
  ]
})
</script>
