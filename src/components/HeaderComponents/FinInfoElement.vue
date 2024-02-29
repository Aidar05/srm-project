<template>
  <div class="header-fin-info">
    <Icon :name="icon"/>

    <span class="header-fin-info-text"> {{ text }} {{ value }} </span>
  </div>
</template>

<script>
import Icon from '../MenuComponents/Icon.vue';

export default{
  name: "FinInfoElemenet",
  props: {
    icon: String,
    text: String,
    value: String
  }
}
</script>

<style>
@import url("../../assets/css/header.css");
</style>