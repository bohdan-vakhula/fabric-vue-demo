<template>
  <div id="app">
    <AppHeader/>
    <div class="main-view">
      <SideBar/>
      <WorkPlace/>
    </div>
  </div>
</template>

<script>
import AppHeader from "./components/header/AppHeader.vue";
import SideBar from "./components/sidebar/SideBar.vue";
import WorkPlace from "./components/workplace/WorkPlace.vue";

export default {
  name: "app",
  components: {
    AppHeader,
    SideBar,
    WorkPlace
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  display: flex;
  height: 100vh;
  flex-direction: column;
  .main-view {
    display: flex;
    width: 100%;
    flex: 1;
  }
}
body {
  margin: 0;
  background: #646464;
}
</style>
