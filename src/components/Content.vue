<template>
  <div class="content-main-container">
    <div class="left-content-container">
      <ContentBtns :contentIcons="contentIcons"/>
  
      <ContentTable :tableData="tableOne" />
  
      <ContentTable :tableData="tableTwo" />
    </div>

    <div class="right-content-container">
      <SalesMap />
    </div>
</div>
</template>

<script>
import Icon from './MenuComponents/Icon.vue';
import ContentBtns from "./ContentComponents/ContentBtns.vue"
import ContentTable from './ContentComponents/ContentTable.vue';
import SalesMap from "./ContentComponents/SalesMap.vue"

export default{
  name: "Content",
  components: {
    Icon, ContentBtns, ContentTable, SalesMap
  },
  data() {
    return {
      contentIcons: [
        {icon: "Repeat"},
        {icon: "CirclePlus"},
        {icon: "List"}
      ],
      tableOne: [
        ["Дата", "Номер", "Операция", "Контрагент", "Касса", "Автор", "Комментарий", "Способ оплаты", "Сумма"], 
        {data: "01.05.2023", id: 17487, operation: "Оплата поставщику", contragent: "ТОО Форстр", checkout: "Шаляпина",
          author: "Макпал", comment: "Излишние", paymentMethod: "Kaspi макпал", sum: 40000, isNegative: false
        }, 
        {data: "01.05.2023", id: 17487, operation: "Оплата поставщику", contragent: "ТОО Форстр", checkout: "Шаляпина",
          author: "Макпал", comment: "Излишние", paymentMethod: "Kaspi макпал", sum: -20000, isNegative: true
        }, 
        {data: "01.05.2023", id: 17487, operation: "Оплата поставщику", contragent: "ТОО Форстр", checkout: "Шаляпина",
          author: "Макпал", comment: "Излишние", paymentMethod: "Kaspi макпал", sum: 40000, isNegative: false
        }, 
        {data: "01.05.2023", id: 17487, operation: "Оплата поставщику", contragent: "ТОО Форстр", checkout: "Шаляпина",
          author: "Макпал", comment: "Излишние", paymentMethod: "Kaspi макпал", sum: -20000, isNegative: true
        }, 
        {data: "01.05.2023", id: 17487, operation: "Оплата поставщику", contragent: "ТОО Форстр", checkout: "Шаляпина",
          author: "Макпал", comment: "Излишние", paymentMethod: "Kaspi макпал", sum: 40000, isNegative: false
        } 
      ], 
      tableTwo: [
        ["Вид оплаты", "Наличные", "Безналичные", "Всего"],
        {paymentType: "Оплата за покупку", cash: "15 645 654", nonCash: "456 665", sum: "212 565 222", '': ''},
        {paymentType: "Оплата за покупку", cash: "15 645 654", nonCash: "456 665", sum: "212 565 222", '': ''},
        {paymentType: "Оплата за покупку", cash: "15 645 654", nonCash: "456 665", sum: "212 565 222", '': ''},
        {paymentType: "Оплата за покупку", cash: "15 645 654", nonCash: "456 665", sum: "212 565 222", '': ''},
        ["Итог", "456 665", "123 123", "4 654 456", '']
      ],
      salesDataOne: [
        {header: "Финансы на", dates: "15.02.2023-21.06.2023"}, 
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/content.css");
</style>