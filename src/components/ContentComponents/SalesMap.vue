<template>
    <div class="sales-map">
      <div class="sales-header-container">
        <span class="sales-header-text"> {{ salesHeader }} 
          <span class="sales-header-date"> {{ salesDates }} </span>
        </span>
      </div>

      <div class="sales-map-elements">
        <div class="sales-map-element" v-for="(item, index) in salesData.slice(1)"
         :key="index" :class="{ profit: item.isProfit }">
          <div class="sales-el-text">
            <span class="sales-el-text"> {{ item.payMethod }}
              <span class="sales-name"> {{ item.name }} </span>
            </span> 
          </div>

          <div class="sales-el-value"> 
            <Icon v-if="item.icon" :name="item.icon"/>

            <span> {{ item.amount }} </span>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import Icon from '../MenuComponents/Icon.vue';

export default{
  name: "SalesMap",
  components: {
    Icon
  },
  props: {
    salesHeader: String,
    salesDates: String,
    salesData: Array
  }
}
</script>