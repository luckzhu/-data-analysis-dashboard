<template>
  <div id="header">
    <div class="logo">
      <img src="../assets/img/logo.png" alt="" />
    </div>
    <ul class="top_nav">
      <li>Support</li>
      <li>Manual</li>
      <li>Notifications</li>
    </ul>
    <div class="search">
      <el-input
        placeholder="Search by keywords…"
        suffix-icon="el-icon-search"
        v-model="topSearch"
      >
      </el-input>
    </div>
    <div class="user_info">
      <div class="user_info_welcome">
        <p>Welcome Chandan!</p>
        <p class="data">
          Monday, 10th May
        </p>
      </div>

      <div class="avatar">
        <img src="../assets/img/avatar.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      topSearch: ""
    };
  }
};
</script>

<style lang="scss" scoped>
#header {
  background: #338bf8;
  padding: 17px 30px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-family: Microsoft YaHei;
  > .logo img {
    width: 150px;
  }
  > .top_nav {
    display: flex;
    margin-left: 30px;
    li {
      color: white;
      line-height: 140%;
      text-align: left;
      margin-right: 23px;
    }
  }
  .search {
    width: 293px;
    height: 38px;
  }

  > .user_info {
    display: flex;
    > .user_info_welcome {
      display: flex;
      flex-direction: column;
      color: white;
      margin-right: 18px;
    }
    > .avatar img {
      width: 44px;
      border-radius: 50%;
      background: white;
    }
  }
}
</style>