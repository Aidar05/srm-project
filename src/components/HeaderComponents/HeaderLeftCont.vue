<template>
  <div class="header-inner-container" id="header-left-contaienr">
    <Icon id="indent-decrease" :name="'IndentDeacrease'"/>
  
    <div class="filials-button">
      <Icon :name="'SmartHome'"/>
    
      <span>Филиалы</span>

      <Icon id="filials-dropdown" :name="'ChevronDown'"/>
    </div>
  </div>
</template>

<script>  
import Icon from '../MenuComponents/Icon.vue';

export default{
  name: "HeaderLeftCont",
  components: {
    Icon
  }
}
</script>