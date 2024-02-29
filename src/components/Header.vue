<template>
  <div id="header-container">
    <div id="header">
      <HeaderLeftCont />

      <HeaderRightCont :exchangeRate="exchangeRate" :finInfo="finInfo"/>
      <!-- <div class="header-inner-container" id="header-right-container">
        <div class="exchange-rate">
          <CurrencyElement v-for="(item, index) in exchangeRate" :key="index"
            :icon="item.icon" :currencyValue="item.currencyValue"/>
        </div>       
        
        <div id="fin-info-container">
          <FinInfoElement v-for="(item, index) in finInfo" :key="index" :icon="item.icon"
            :text="item.icon" :value="item.value" :bgColor="item.bgColor ? item.bgColor : 'default'"/>
        </div>
      </div> -->
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
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/header.css");
</style>