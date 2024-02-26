<template>
  <div class="menu-container" id="dashboard">
    <DashboardElement :dashboard_text='dashboardTextAdd' icon="CirclePlus" id="dashboard-add">
      <template #default>
        <Icon id="dashboard-dropdown-icon" :name="'ChevronDown'" />
      </template>
    </DashboardElement>

    <DashboardElement :dashboard_text='dashboardTextOne' icon="Point" class="active" />

    <DashboardElement :dashboard_text=dashboardTextTwo icon="Point"/>
  </div>
</template>

<script>
import DashboardElement from './DashboardElement.vue';
import Icon from './Icon.vue';

export default{
  name: "DashboardContainer",
  components: {
    DashboardElement, Icon
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