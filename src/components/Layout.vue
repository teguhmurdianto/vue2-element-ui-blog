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
        <el-menu-item index="3">Orders</el-menu-item>
      </el-menu>
    </el-container>
  </el-header>
  <el-main>Main</el-main>
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
      activeIndex2: "1"
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
};
</script>
<style lang="scss" scoped>
.el-header {
  width: 100%;
  height: 60px;
  position: fixed;
  background: #39454b;
  color: rgba(185, 186, 187, 0.5);
}
.el-menu {
  background: transparent;
  top: 0;
}
.el-main {
  margin-top: 60px;
  height: 1300px;
}
.el-footer {
  position: relative;
  height: 5em;
  line-height: 5em;
  margin: 0;
  background: #39454b;
  color: rgba(185, 186, 187, 0.5);
  overflow: hidden;
}
</style>
