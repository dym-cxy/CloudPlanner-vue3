<template>
  <div id="app">
    <el-form :model="form" label-width="120px">
      <el-form-item label="任务标题">
        <el-input v-model="form.taskTitle" placeholder="标题是什么呢"></el-input>
      </el-form-item>
      <el-form-item label="任务详情">
        <el-input v-model="form.taskDetail" placeholder="内容是什么呢"></el-input>
      </el-form-item>
      <el-form-item label="优先级">
        <el-radio-group v-model="form.priority">
          <el-radio label="急">急</el-radio>
          <el-radio label="较急">较急</el-radio>
          <el-radio label="缓">缓</el-radio>
        </el-radio-group>
      </el-form-item>
      <el-form-item label="开始日期">
        <el-date-picker
            v-model="form.startDate"
            type="date"
            placeholder="选择开始日期">
        </el-date-picker>
      </el-form-item>
      <el-form-item label="开始时间">
        <el-time-picker
            v-model="form.startTime"
            placeholder="选择开始时间">
        </el-time-picker>
      </el-form-item>
      <el-form-item label="结束日期">
        <el-date-picker
            v-model="form.endDate"
            type="date"
            placeholder="选择结束日期">
        </el-date-picker>
      </el-form-item>
      <el-form-item label="结束时间">
        <el-time-picker
            v-model="form.endTime"
            placeholder="选择结束时间">
        </el-time-picker>
      </el-form-item>
      <el-form-item>
        <el-button type="primary" @click="submitForm">提交</el-button>
        <el-button @click="resetForm">重置</el-button>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        taskTitle: '',
        taskDetail: '',
        priority: '',
        startDate: '',
        startTime: '',
        endDate: '',
        endTime: ''
      }
    };
  },
  methods: {
    submitForm() {
      // 这里可以添加提交表单的逻辑，例如发送数据到后端
      console.log('提交的数据:', this.form);
    },
    resetForm() {
      // 重置表单数据
      this.form = {
        taskTitle: '',
        taskDetail: '',
        priority: '',
        startDate: '',
        startTime: '',
        endDate: '',
        endTime: ''
      };
    }
  }
};
</script>

<style>
#app {
  background-color: #e0e8f2;
}
</style>