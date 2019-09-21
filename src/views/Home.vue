<template>
  <div class="home">
    <el-container>
      <el-header height="auto"><Header></Header></el-header>
      <el-container>
        <el-aside width="auto"><Sidebar></Sidebar></el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import Header from "../components/Header";
import Sidebar from "../components/Sidebar";
export default {
  name: "home",
  components: { Header, Sidebar }
};
</script>
<style lang="scss" scoped>
.el-header {
  padding: 0;
}
</style>
