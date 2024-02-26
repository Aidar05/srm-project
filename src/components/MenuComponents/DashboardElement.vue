<template>
  <div class="menu-element">  
    <Icon class="menu-left-icon" :name="icon" />

    <span class="menu-element-text">{{ dashboard_text }}</span>
    <slot id="dashboard-dropdown-icon"></slot>
  </div>

</template>

<script>
import Icon from './Icon.vue';

export default {
  name: "DashboardElement",
  components: {
    Icon
  },
  props: {
    dashboard_text: String,
    icon: String,
  }
}
</script>

<style>
@import url("../../assets/css/menu.css");
</style>