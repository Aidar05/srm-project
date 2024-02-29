<template>
  <div class="header-inner-container" id="header-right-container">
    <div class="exchange-rate">
      <CurrencyElement v-for="(item, index) in exchangeRate" :key="index"
        :icon="item.icon" :currencyValue="item.currencyValue"/>
    </div>       
    
    <div id="fin-info-container">
      <FinInfoElement v-for="(item, index) in finInfo" :key="index" :icon="item.icon"
        :text="item.icon" :value="item.value" :bgColor="item.bgColor ? item.bgColor : 'default'"/>
    </div>
  </div>
</template>

<script>
import CurrencyElement from './CurrencyElement.vue';
import FinInfoElement from './FinInfoElement.vue';

export default{
  name: "HeaderRightCont",
  components: {
    CurrencyElement, FinInfoElement
  },
  props: {
    exchangeRate: Object,
    finInfo: Object
  }
}
</script>