<template>
  <div class="menu-element">  
    <!-- <svg class="dashboard-left-icon point-icon" width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
      <circle cx="10.0001" cy="10" r="3.33333" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
    </svg> -->
    <!-- <inline-svg :src="require(`../../assets/icons/${icon}.svg`)"/> -->
    <Icon :name="icon" />

    <span class="dashboard-element-text">{{ dashboard_text }}</span>
  </div>

</template>

<script>
import Icon from './Icon.vue';

export default {
  name: "MenuElement",
  components: {
    Icon
  },
  props: {
    dashboard_text: String,
    icon: String,
  }
}

</script>