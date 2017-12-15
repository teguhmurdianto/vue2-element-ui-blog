<<template>
<div class="layout">
  <transition name="aside-fade">
    <el-aside v-if="isShowSidebar">
    </el-aside>
  </transition>

  <el-container :class="{'el-container-aside': isShowSidebar}">
    <el-header>
      <i class="el-icon-setting" v-on:click="showSidebar"></i>
    </el-header>

    <el-main>
      <el-table :data="tableData">
        <el-table-column prop="date" label="Date" width="140">
        </el-table-column>
        <el-table-column prop="name" label="Name" width="120">
        </el-table-column>
        <el-table-column prop="address" label="Address">
        </el-table-column>
      </el-table>
    </el-main>

    <el-footer>Footer</el-footer>
  </el-container>
</div>
</template>

<script>
export default {
  name: "Layout",
  data() {
    const item = {
      date: '2016-05-02',
      name: 'Tom',
      address: 'No. 189, Grove St, Los Angeles'
    };
    return {
      isShowSidebar: false,
      tableData: Array(20).fill(item)
    }
  },
  methods: {
    showSidebar: function(event) {
      this.isShowSidebar = !this.isShowSidebar;
    }
  }
};
</script>

<style>
.el-container {
  height: 100%;
  border: 1px solid #eee;
  transition: 0.5s;
  background-color: rgb(238, 241, 246);
}

.el-container-aside {
  margin-left: 300px;
}

.el-aside {
  color: #333;
  width: 200px;
  background-color: rgb(238, 241, 246);
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  left: 0;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
}

.aside-fade-enter-active {
  transition: opacity 0.1s, transform 0.3s cubic-bezier(0.17, -0.65, 0.665, 1.25);
}

.aside-fade-leave-active {
  transition: opacity 0.1s, transform 0.3s cubic-bezier(0.17, -0.65, 0.665, 1.25);
}

.aside-fade-enter,
.aside-fade-enter-to{
  transition: opacity 0.1s, transform 0.3s cubic-bezier(0.17, -0.65, 0.665, 1.25);
}

.aside-fade-leave,
.aside-fade-leave-to {
  transition: opacity 0.1s, transform 0.3s cubic-bezier(0.17, -0.65, 0.665, 1.25);
}

.el-header {
  background-color: #B3C0D1;
  color: #333;
  line-height: 60px;
  text-align: left;
  font-size: 12px;
  position: fixed;
  width: 100%;
  overflow: hidden;
  top: 0px;
  z-index: 1;
}

.el-main {
  padding: 60px 0px 60px 0px;
}

.el-footer {
  background-color: #B3C0D1;
  color: #333;
  line-height: 60px;
  text-align: left;
  font-size: 12px;
  position: fixed;
  width: 100%;
  overflow: hidden;
  bottom: 0px;
  z-index: 1;
}

/* .el-row {
  margin-bottom: 20px;
  &:last-child {
    margin-bottom: 0;
  }
}

.el-col {
  border-radius: 4px;
}

.bg-purple-dark {
  background: #99a9bf;
}

.bg-purple {
  background: #d3dce6;
}

.bg-purple-light {
  background: #e5e9f2;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
}

.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
} */

.el-icon-setting {
  cursor: pointer;
  font-size: 30px;
  vertical-align: middle;
}
</style>
