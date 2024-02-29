<template>
  <div id="header-container">
    <div id="header">
      <div class="header-inner-container" id="header-left-contaienr">
        <Icon id="indent-decrease" :name="'IndentDeacrease'"/>
      
        <div class="filials-button">
          <Icon :name="'SmartHome'"/>
        
          <span>Филиалы</span>

          <Icon id="filials-dropdown" :name="'ChevronDown'"/>
        </div>
      </div>

      <div class="header-inner-container" id="header-right-container">
        <div class="exchange-rate">
          <CurrencyElement v-for="(item, index) in exchangeRate" :key="index"
            :icon="item.icon" :currencyValue="item.currencyValue"/>
        </div>       
        
        <div id="fin-info-container">
          <FinInfoElement v-for="(item, index) in finInfo" :key="index"
            :icon="item.icon" :text="item.text" :value="item.value" />
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
import FinInfoElement from './HeaderComponents/FinInfoElement.vue';

export default{
  name: "Header",
  components: {
    Icon, CurrencyElement, FinInfoElement
  },
  data() {
    return {
      exchangeRate: [
        {icon: "CurrencyDollar", currencyValue: "54.82"},
        {icon: "CurrencyEuro", currencyValue: "54.82"},
        {icon: "CurrencyRubel", currencyValue: "54.82"},
        {icon: "CurrencyYen", currencyValue: "54.82"},
      ],
      finInfo: [
        {icon: "ArrowDown", text: "Нам должны:", value: "808450"},
        {icon: "ArrowUp", text: "Мы должны:", value: "1229822"},
        {icon: "UsdCircle", text: "Касса. Наличные", value: "+131 983"},
        {icon: "UsdCircle", text: "Касса. Безнал", value: "+2 337 836"}
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/header.css");
</style>