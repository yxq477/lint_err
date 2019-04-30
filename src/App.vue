<template>
  <div>
    <el-upload
      action="https://jsonplaceholder.typicode.com/posts/"
      list-type="picture-card"
      :on-remove="handleRemove">
      <i class="el-icon-plus"></i>
    </el-upload>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import { ElUploadInternalFileDetail } from 'element-ui/types/upload';

export default Vue.extend({
  name: 'app',
  methods: {
    handleRemove(file: ElUploadInternalFileDetail, fileList:File[]) {
      console.log(file, fileList);
    },
  },
});
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
