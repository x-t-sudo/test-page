<template>
  <div id="nav">
    <el-menu
      :default-active="activeIndex2"
      class="el-menu-demo"
      mode="horizontal"
      router="true"
      @select="handleSelect"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b"
    >
      <el-menu-item index="1" route="/">主页</el-menu-item>
      <el-submenu index="2">
        <template #title>网页工具</template>
        <el-menu-item index="2-1" route="/SimulatedRequest">模拟请求</el-menu-item>
      </el-submenu>
    </el-menu>
  </div>
  <router-view />
</template>
<script>
export default {
  data() {
    return {
      activeIndex: "1",
      activeIndex2: "1",
    };
  },
  methods: {
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
* {
  margin: 0px;
  padding: 0px;
}
</style>
