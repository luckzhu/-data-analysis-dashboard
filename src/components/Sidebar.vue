<template>
  <div id="siderbar">
    <!-- <el-radio-group v-model="isCollapse" style="margin-bottom: 20px;">
      <el-radio-button :label="false" @click="allOpen">展开</el-radio-button>
      <el-radio-button :label="true" @click="allClose">收起</el-radio-button>
    </el-radio-group> -->
    <el-menu
      default-active="1-1"
      :default-openeds="openeds"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      :collapse="isCollapse"
    >
      <el-submenu index="1">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span slot="title">Dashboard</span>
        </template>
        <el-menu-item index="1-1">Overview</el-menu-item>
        <el-menu-item index="1-2">Reports</el-menu-item>
        <el-menu-item index="1-3">Status</el-menu-item>
      </el-submenu>

      <el-submenu index="2">
        <template slot="title">
          <i class="el-icon-document"></i>
          <span slot="title">Statistics</span>
        </template>
        <el-menu-item index="2-1">Page Analytics</el-menu-item>
        <el-menu-item index="2-2">Options</el-menu-item>
        <el-menu-item index="2-3">Tickets</el-menu-item>
        <el-menu-item index="2-4">Tickets</el-menu-item>
        <el-menu-item index="2-5">Manage Plans</el-menu-item>
        <el-menu-item index="2-6">Manage Users</el-menu-item>
      </el-submenu>

      <el-submenu index="3">
        <template slot="title">
          <i class="el-icon-setting"></i>
          <span slot="title">Others</span>
        </template>
        <el-menu-item index="3-1">Notifications</el-menu-item>
        <el-menu-item index="3-2">Settings</el-menu-item>
        <el-menu-item index="3-3">Help</el-menu-item>
      </el-submenu>
    </el-menu>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isCollapse: false,
      openeds:['1','2','3']
    };
  },
  created(){
    this.handleOpen()
  },
  methods: {
    handleOpen(key, keyPath) {
      console.log(key, keyPath);
    },
    handleClose(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>

<style lang="scss" scoped>
#siderbar {
  background: rgb(255, 255, 255);
  overflow-x: hidden;
  min-width: 220px;
  border-right: 1px solid #d8d8d8;
  box-shadow: 1px 1px 2px 2px #d8d8d8;
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 100%;
  }

  .el-submenu {
    padding: 10px 0;
    &:not(:last-child) {
      border-bottom: 1px solid #d8d8d8;
    }
  }
}
</style>