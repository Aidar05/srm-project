<template>
  <div class="dashboard-element">  
    <svg class="dashboard-left-icon" width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
      <circle cx="12.5" cy="12" r="9" stroke="#4B465C" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
      <circle cx="12.5" cy="12" r="9" stroke="white" stroke-opacity="0.2" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
      <path d="M9.5 12H15.5" stroke="#4B465C" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
      <path d="M9.5 12H15.5" stroke="white" stroke-opacity="0.2" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
      <path d="M12.5 9V15" stroke="#4B465C" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
      <path d="M12.5 9V15" stroke="white" stroke-opacity="0.2" stroke-width="1.75" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>

    <span class="dashboard-element-text">{{ dashboard-text }}</span>
  </div>

</template>

<script>
export default {
  name: "DashboardElement",
  props: ['dasboard-text']
}

</script>