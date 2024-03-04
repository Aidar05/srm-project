<template>
  <div id="header-container">
    <div id="header">
      <HeaderLeftCont />

      <HeaderRightCont :exchangeRate="exchangeRate" :finInfo="finInfo"
       :iconsContainer="iconsContainer"/>
    </div>

    <div id="nav-tabs">
      <NavElement v-for="(item, index) in navContainer" :key="index"
       :navText="item.text" :activeNav="item.activeNav"/>
    </div>
  </div>
</template>

<script>
import HeaderLeftCont from './HeaderComponents/HeaderLeftCont.vue';
import HeaderRightCont from './HeaderComponents/HeaderRightCont.vue';
import NavElement from './HeaderComponents/NavElement.vue';
import Icon from './MenuComponents/Icon.vue';

export default{
  name: "Header",
  components: {
    Icon, HeaderLeftCont, HeaderRightCont, NavElement
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
      ],
      navContainer: [
        {text: "Active", activeNav: true},
        {text: "Links", activeNav: false},
        {text: "Links", activeNav: false},
        {text: "Links", activeNav: false}
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/header.css");
</style>