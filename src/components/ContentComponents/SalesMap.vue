<template>
    <div class="sales-map">
      <div class="sales-header-container">
        <span class="sales-header-text"> {{ salesHeader }} 
          <span class="sales-header-date"> {{ salesDates }} </span>
        </span>
      </div>

      <div class="sales-map-elements">
        <div class="sales-map-element">
          <div class="sales-el-text">
            <span class="sales-el-text"> {{ payMethod }}
              <span class="sales-name"> {{ name }} </span>
            </span> 
          </div>

          <div class="sales-el-value"> 
            <Icon :name="icon"/>

            <span> {{ amount }} </span>
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
    // salesHeader: String,
    // salesDates: String,
    // payMethod: String,
    // name: String,
    // amount: String,
    // icon: String
    salesData: Array
  }
}
</script>