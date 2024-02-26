<template>
  <div id="left-menu">
    <div id="logo-container">
      <div id="logo"></div>      

      <span id="logo-text">AlloMaster</span>
    </div>

    <div class="menu-container" id="dashboard">
      <MenuElement :dashboard_text='dashboardTextAdd' icon="CirclePlus" id="dashboard-add" />

      <MenuElement :dashboard_text='dashboardTextOne' icon="Point" class="active" />

      <MenuElement :dashboard_text=dashboardTextTwo icon="Point"/>
    </div>
  </div>

</template>

<script>
import MenuElement from "./MenuComponents/MenuElement.vue"

export default{
  name: "Menu",
  components: {
    MenuElement
  }, 
  data() {
    return {
      dashboardTextAdd: "Добавить",
      dashboardTextOne: "Новый ремонт",
      dashboardTextTwo: "Новая продажа"
    }
  }
}
</script>

<style>
@import url("../assets/css/menu.css");

</style>