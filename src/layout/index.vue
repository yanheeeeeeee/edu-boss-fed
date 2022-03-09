<template>
  <div class="layout">
    <el-container>
      <el-aside width="200px">
        <app-aside></app-aside>
      </el-aside>
      <el-container>
        <el-header>Header</el-header>
        <el-main>
          <!-- 子路由出口 -->
          <router-view />
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'
import AppAside from './components/AppAside/index.vue'
@Component({
  components: {
    AppAside
  }
})
export default class Layout extends Vue {}
</script>

<style lang="scss">
.el-container {
  min-height: 100vh;
  // min-width: 980px;
}

.el-aside {
  background: #d3dce6;
}

.el-header {
  background: #fff;
}

.el-main {
  background: #e9eef3;
}
</style>
