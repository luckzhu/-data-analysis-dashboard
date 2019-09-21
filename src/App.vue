<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "app",
  components: {}
};
</script>

<style>
@import "./assets/css/normalize.css";
#app {
}
.search .el-input,
.search .el-input__inner {
  background: rgba(0, 0, 0, 0.06315104166666667);
  border: 1px solid rgba(179, 179, 179, 0.063);
  border-radius: 100px;
  color: #fff;
}
.search .el-input__inner:hover,
.search .el-input__inner:focus{
  border: 1px solid rgb(255, 255, 255);
}
</style>
