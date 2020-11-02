<template>
  <div id="app">
    <!-- keepalive保存当前页面 -->
    <keep-alive>
      <router-view v-if="$route.meta.keepalive" />
    </keep-alive>
    <router-view v-if="!$route.meta.keepalive" />
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  background-color: #f4f4f4;
}
p {
  margin: 0;
}
</style>
