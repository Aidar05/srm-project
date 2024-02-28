<template>
  <div id="header-container">
    <div id="header">
      <div id="header-left-contaienr">
        <Icon id="indent-decrease" :name="'IndentDeacrease'"/>
      
        <div class="filials-button">
          <Icon :name="'SmartHome'"/>
        
          <span>Филиалы</span>

          <Icon id="filials-dropdown" :name="'ChevronDown'"/>
        </div>
      </div>
    </div>

    <div id="nav-tabs"></div>
  </div>

  <div id="content">

  </div>
</template>

<script>
import Icon from './MenuComponents/Icon.vue';

export default{
  name: "Header",
  components: {
    Icon
  }
}
</script>

<style>
@import url("../assets/css/header.css");
</style>