<template>
  <div>
<!--头部区域开始-->
    <div style="height: 60px;display: flex;">
     <div style="width: 240px;display: flex;align-items: center;padding-left:20px;background-color:#3a456b">
       <img style="width: 40px;height: 40px; border-radius:50%" src="@/assets/imgs/生成系统%20Logo.png" alt="">
       <span style="font-size: 20px;font-weight: bold;color: #e6e6e6;margin-left: 5px">后台管理系统</span>
     </div>
      <div style="flex:1;display: flex;align-items: center;padding-right:20px;border-bottom:1px solid #ddd">
        首页/流水分析
      </div>
      <div style="width: fit-content; ;padding-right: 20px;display:flex;align-items: center;border-bottom:1px solid #ddd">
        <el-dropdown>
          <div style="display: flex;align-items:center">
            <img style="width: 40px; height: 40px; border-redius:50%" src="https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png" alt="">
            <span style="margin-left: 5px">管理员</span>
          </div>
          <template #dropdown>
            <el-dropdown-menu>
              <el-dropdown-item>个人信息</el-dropdown-item>
              <el-dropdown-item>修改密码</el-dropdown-item>
              <el-dropdown-item>退出登录</el-dropdown-item>
            </el-dropdown-menu>
          </template>
        </el-dropdown>
      </div>
    </div>

<!--头部区域结束-->
<!--下方区域开始-->
  <div style="display: flex">
    <!--菜单区域开始-->
    <div style="width: 240px;">
      <el-menu router :default-openeds="['1']":default-active="router.currentRoute.value.path"style="min-height:calc(100vh - 60px)">
        <el-menu-item index="/manager/home">
          <el-icon><House /></el-icon>
          <span>首页</span>
        </el-menu-item>
        <el-sub-menu index="1">
          <template #title>
          <el-icon><location /></el-icon>
          <span>账务管理</span>
        </template>
          <el-menu-item index="test">
            <el-icon><Compass /></el-icon>
            查询统计
          </el-menu-item>
          <el-menu-item index="/manager/about">
            <el-icon><Edit /></el-icon>
            记账
          </el-menu-item>
          </el-sub-menu>
      </el-menu>
    </div>
    <!--菜单区域结束-->
    <!--数据渲染区域开始-->
    <div style="flex: 1;width: 0; padding: 10px; background:#f2f4ff">
      <RouterView/>
    </div>
    <!--数据渲染区域结束-->
  </div>
    <!--下方区域结束-->


  </div>
</template>
<script setup>

import router from "@/router/index.js";
</script>
<style>
.el-menu{
  background-color: #3a456b;
  border:none;
  box-shadow:0 0 8px rgba(0,0,0,12);

}
.el-sub-menu__title{
  background-color:#3a456b;
  color: #dddddd;
}
.el-menu-item{
  height: 50px;
  color: #dddddd;
}
.el-menu .is-active {
  background-color: #537bee;
  color:#fff;
}
.el-sub-menu__title:hover{
  background-color:#3a456b;
}
.el-menu-item:not(.is-active):hover{
  background-color: #7a9fff;
  color: #333333;
}
.el-dropdown{
  cursor:pointer;
}
.el-tooltip__trigger{
  outline: none;
}
.el-menu--inline.el-menu-item{
  padding-left: 48px !important;
}
</style>

