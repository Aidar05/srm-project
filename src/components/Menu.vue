<template>
  <div id="left-menu">
    <div id="logo-container">
      <div id="logo"></div>      

      <span id="logo-text">AlloMaster</span>
    </div>

    <div id="dashboard">
      <div class="dashboard-element" id="dashboard-add">  
        <svg class="dashboard-left-icon" width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="12.5" cy="12" r="9" stroke="#4B465C" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
          <circle cx="12.5" cy="12" r="9" stroke="white" stroke-opacity="0.2" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M9.5 12H15.5" stroke="#4B465C" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M9.5 12H15.5" stroke="white" stroke-opacity="0.2" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M12.5 9V15" stroke="#4B465C" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M12.5 9V15" stroke="white" stroke-opacity="0.2" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>

        <span id="dashboard-add-text">Добавить</span>
  
        <svg id="dashboard-dropdown-icon" width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M4.5 6.75L9 11.25L13.5 6.75" stroke="#4B465C" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M4.5 6.75L9 11.25L13.5 6.75" stroke="white" stroke-opacity="0.2" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>

      </div>

      <DashboardElement dashboard-text='dashboardTextOne' class="active" />

      <DashboardElement :dashboard-text=dashboardTextTwo />
    </div>
  </div>

</template>

<script>
import DashboardElement from "./MenuComponents/DashboardElement.vue"

export default{
  name: "Menu",
  components: {
    DashboardElement
  }, 
  data() {
    return {
      dashboardTextOne: "Новый ремонт",
      dashboardTextTwo: "Новая продажа"
    }
  }
}
</script>

<style>
@import url("../assets/css/menu.css");

</style>