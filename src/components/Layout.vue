<template>
<div class="layout">
<el-container>
  <el-header>
    <el-container>
      <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
        <el-menu-item index="1">Processing Center</el-menu-item>
        <el-submenu index="2">
          <template slot="title">Workspace</template>
          <el-menu-item index="2-1">item one</el-menu-item>
          <el-menu-item index="2-2">item two</el-menu-item>
          <el-menu-item index="2-3">item three</el-menu-item>
        </el-submenu>
        <el-menu-item index="3"><a href="https://www.ele.me" target="_blank">Orders</a></el-menu-item>
      </el-menu>
    </el-container>
  </el-header>
  <el-main>
    <el-row>
      <el-col :span="8" v-for="(o, index) in 2" :key="o" :offset="index > 0 ? 2 : 0">
        <el-card :body-style="{ padding: '0px' }">
          <img src="/static/images/hamburger.png" class="image">
          <div style="padding: 14px;">
            <span>Yummy hamburger</span>
            <div class="bottom clearfix">
              <time class="time">{{ currentDate }}</time>
              <el-button type="text" class="button">Operating button</el-button>
            </div>
          </div>
        </el-card>
      </el-col>
    </el-row>
  </el-main>
  <el-footer>Footer</el-footer>
</el-container>
</div>
</template>

<script>
export default {
  name: "Layout",
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1",
      currentDate: new Date()
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>
<style lang="scss">
.layout .el-container {
  .el-header {
    width: 100%;
    height: 100px;
    padding: 0;
    .el-container .el-menu {
      width: 100%;
      vertical-align: middle;
      background: transparent;
    }
  }
  .el-main {
    height: 1300px;
    padding: 20px 0 0 0;
  }
  .el-footer {
    position: relative;
    height: 100px;
    line-height: 100px;
    margin: 0;
    overflow: hidden;
  }

  .time {
    font-size: 13px;
    color: #999;
  }

  .bottom {
    margin-top: 13px;
    line-height: 12px;
  }

  .button {
    padding: 0;
    float: right;
  }

  .image {
    width: 100%;
    display: block;
  }

  .clearfix:before,
  .clearfix:after {
    display: table;
    content: "";
  }

  .clearfix:after {
    clear: both;
  }
}
</style>
