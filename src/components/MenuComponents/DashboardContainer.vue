<template>
  <div class="menu-container" id="dashboard">
    <MenuElement :dashboard_text='dashboardTextAdd' icon="CirclePlus" id="dashboard-add">
      <template #default>
        <Icon id="dashboard-dropdown-icon" :name="'ChevronDown'" />
      </template>
    </MenuElement>

    <MenuElement :dashboard_text='dashboardTextOne' icon="Point" class="active" />

    <MenuElement :dashboard_text=dashboardTextTwo icon="Point"/>
  </div>
</template>

<script>
import MenuElement from './MenuElement.vue';
import Icon from './Icon.vue';

export default{
  name: "DashboardContainer",
  components: {
    MenuElement, Icon
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