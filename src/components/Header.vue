<template>
  <div id="header-container">
    <div id="header">
      <HeaderLeftCont />

      <HeaderRightCont :exchangeRate="exchangeRate" :finInfo="finInfo" :iconsContainer="iconsContainer"/>
    </div>

    <div id="nav-tabs"></div>
  </div>

  <div id="content">

  </div>
</template>

<script>
import HeaderLeftCont from './HeaderComponents/HeaderLeftCont.vue';
import HeaderRightCont from './HeaderComponents/HeaderRightCont.vue';
import Icon from './MenuComponents/Icon.vue';

export default{
  name: "Header",
  components: {
    Icon, HeaderLeftCont, HeaderRightCont
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
        {icon: "ArrowDownRight", text: "Нам должны: ", value: "46808450", bgColor: "red"},
        {icon: "ArrowUpRight", text: "Мы должны: ", value: "1229822", bgColor: "green"},
        {icon: "CircleUSD", text: "Касса. Наличные ", value: "+131 983"},
        {icon: "CircleUSD", text: "Касса. Безнал ", value: "+2 337 836"}
      ], 
      iconsContainer: [
        {icon: "AccessPoint"},
        {icon: "CircleUSD"},
        {icon: "Bell"}
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/header.css");
</style>