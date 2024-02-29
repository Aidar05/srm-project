<template>
  <div class="header-fin-info" :class="bgColor">
    <span class="header-fin-info-text">
      <Icon :name="icon"/>
    
      {{ text }}
    </span>

    <span class="header-fin-info-value"> {{ value }} </span>
  </div>
</template>

<script>
import Icon from '../MenuComponents/Icon.vue';

export default{
  name: "FinInfoElemenet",
  components: {
    Icon
  },
  props: {
    icon: String,
    text: String,
    value: String,
    bgColor: String
  }
}
</script>

<style>
@import url("../../assets/css/header.css");
</style>