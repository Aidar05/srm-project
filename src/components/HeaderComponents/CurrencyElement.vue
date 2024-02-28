<template>
  <div id="currency-element">
    <Icon :name="icon"/>

    <span id="currency-value"> {{ currencyValue }} </span>
  </div>
</template>

<script>
import Icon from '../MenuComponents/Icon.vue';

export default{
  name: "CurrencyElement",
  components: {
    Icon
  },
  props:{
    icon: String,
    currencyValue: String
  }
}
</script>

<style>
@import url("../../assets/css/header.css");
</style>