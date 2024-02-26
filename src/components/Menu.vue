<template>
  <div id="left-menu">
    <div id="logo-container">
      <div id="logo"></div>      

      <span id="logo-text">AlloMaster</span>
    </div>

    <DashboardContainer />
  </div>

</template>

<script>
import DashboardContainer from './MenuComponents/DashboardContainer.vue';

export default{
  name: "Menu",
  components: {
    DashboardContainer
  }
}
</script>

<style>
@import url("../assets/css/menu.css");

</style>