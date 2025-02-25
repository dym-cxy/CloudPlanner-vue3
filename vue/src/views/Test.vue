
<script setup>
import 'vue-cal/dist/vuecal.css';
import VueCal from 'vue-cal';
</script>


<template>


  <div class="div1">

    <div class="div2" >
      <vue-cal
          class="vuecal--blue-theme"
          :events="events"
          locale="zh-cn"
          active-view="month"
          show-time-in-cells
          style="height: 60vh"
      />
    </div>



    <el-carousel height="34vh" motion-blur type="card" class="test3">
      <el-carousel-item v-for="item in 4" :key="item" class="eli">
        <h1>这是个内容</h1>
      </el-carousel-item>
    </el-carousel>


  </div>
</template>


<style>

.div1 {
  background-color: rgb(228, 239, 255);
}

.eli {
  background-color: rgb(190, 215, 255);
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}


.test3 {
  background-color: #fffefe;

}

.h {
  align-items: center;
  justify-content: center;

}
</style>

