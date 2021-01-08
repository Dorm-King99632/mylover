<template>
  <el-container class="main_container">
    <!--头部布局-->
    <el-header>
      <div class="left_box">
        <img src="../assets/img/timg.gif">
        <span>鹦鹉和鲨鱼</span>
      </div>
      <div class="right_box">
        <el-dropdown>
          <img src="../assets/img/timg.gif">
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item icon="el-icon-house">系统首页</el-dropdown-item>
            <el-dropdown-item icon="el-icon-ship">交流讨论</el-dropdown-item>
            <el-dropdown-item icon="el-icon-switch-button">退出登录</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
    </el-header>
    <el-container>
      <el-aside width="200px">Aside</el-aside>
      <el-main>Main</el-main>
    </el-container>
  </el-container>
</template>

<script>
export default {
  name: 'Main'
}
</script>

<style lang="less" scoped>

.main_container {
  height: 100%;
}

.el-header {
  background-color: #B3C0D1;
  color: #333;
  display: flex;
  justify-content: space-between;
  padding-left: 0;
  align-items: center;
  font-size: 20px;

  .left_box { //需在 style 中加入 lang="less" 否则报错
    display: flex;
    align-items: center;

    img {
      width: 60px;
      height: 60px;
      margin: 0 0 10px 15px;
    }

    span {
      margin-left: 15px;
    }

  }
  .right_box {
    .el-dropdown>img {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background-color: #FFFFFF;
      margin: 0 15px 0 0;
      background-size: contain;
    }
  }

}

.el-aside {
  background-color: #D3DCE6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #E9EEF3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

/*下拉菜单样式*/
.el-dropdown-link {
  cursor: pointer;
  color: #409EFF;
}
.el-icon-arrow-down {
  font-size: 12px;
}

</style>
