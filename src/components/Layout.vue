<template>
  <div class="layout">
    <el-container>
      <el-aside width="200px">
        <left-sidebar></left-sidebar>
      </el-aside>
      <el-container>
        <el-header>
          <top-navbar></top-navbar>
        </el-header>
        <el-main>Main</el-main>
        <el-footer>Footer</el-footer>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import TopNavbar from './TopNavbar.vue'
import LeftSidebar from './LeftSidebar.vue'
export default {
  name: 'Layout',
  components: {
    TopNavbar,
    LeftSidebar
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    }
  }
}
</script>

<style>
  .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }

  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 4000px;
  }

  body > .el-container {
    margin-bottom: 0px;
  }
</style>
