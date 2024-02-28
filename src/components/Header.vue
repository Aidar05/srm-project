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

      <div id="header-right-container">
        <div class="exchange-rate">
          <CurrencyElement v-for="(item, index) in exchangeRate" :key="index"
            :icon="item.icon" :currencyValue="item.currencyValue"/>
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
import CurrencyElement from "./HeaderComponents/CurrencyElement.vue"

export default{
  name: "Header",
  components: {
    Icon, CurrencyElement
  },
  data() {
    return {
      exchangeRate: [
        {icon: "CurrencyDollar", currencyValue: "54.82"},
        {icon: "CurrencyEuro", currencyValue: "54.82"},
        {icon: "CurrencyRubel", currencyValue: "54.82"},
        {icon: "CurrencyYen", currencyValue: "54.82"},
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/header.css");
</style>