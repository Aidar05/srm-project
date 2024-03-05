<template>
  <div class="content-main-container">
    <div class="left-content-container">
      <ContentBtns :contentIcons="contentIcons"/>
  
      <div class="content-header-container">
        <div class="content-header-left">
          <ContentBtns :contentIcons="buttonGroup"/>

          <DatePicker />
        </div>

        <div class="search-container">
          <input class="search" type="search" placeholder="Поиск"></input>

          <Icon :name="'ZoomOut'" class="search-img"/>
        </div>
      </div>

      <ContentTable :tableData="tableOne" />
  
      <ContentTable :tableData="tableTwo" :isSecond="true"/>
    </div>

    <div class="right-content-container">
      <SalesMap :salesHeader="salesDataOne[0].header" :salesDates="salesDataOne[0].dates"
       :salesData="salesDataOne"/>
      
      <SalesMap :salesHeader="salesDataTwo[0].header" :salesDates="salesDataTwo[0].dates"
      :salesData="salesDataTwo"/>
    </div>
</div>
</template>

<script>
import Icon from './MenuComponents/Icon.vue';
import ContentBtns from "./ContentComponents/ContentBtns.vue"
import ContentTable from './ContentComponents/ContentTable.vue';
import SalesMap from "./ContentComponents/SalesMap.vue"
import DatePicker from './ContentComponents/DatePicker.vue';

export default{
  name: "Content",
  components: {
    Icon, ContentBtns, ContentTable, SalesMap, DatePicker
  },
  data() {
    return {
      contentIcons: [
        {icon: "Repeat"},
        {icon: "CirclePlus"},
        {icon: "List"}
      ],
      buttonGroup: [
        {text: "C"},
        {text: "B"},
        {text: "-"},
        {text: "+"}
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
        {payMethod: "Наличные", name: "", icon: "ChevronUp", amount: "369 383", isProfit: true},
        {payMethod: "Kaspi", name: "Акылжан", icon: "ChevronUp", amount: "546 596", isProfit: true},
        {payMethod: "Kaspi", name: "Адылжан", icon: "ChevronUp", amount: "770 092", isProfit: true},
        {payMethod: "Kaspi", name: "Мейржан", icon: "ChevronUp", amount: "17 000", isProfit: true},
        {payMethod: "QR", name: "Diler-kz", icon: "ChevronUp", amount: "154 200", isProfit: true},
        {payMethod: "QR", name: "Qastek", icon: "ChevronUp", amount: "339 850", isProfit: true},
        {payMethod: "QR", name: "Sherkhan", icon: "ChevronUp", amount: "888 008", isProfit: true},
        {payMethod: "Безналичные", name: "", icon: "ChevronUp", amount: "1 500", isProfit: false},
        {payMethod: "Безналичные", name: "", icon: "ChevronUp", amount: "227 240", isProfit: true},
        {payMethod: "Итого", name: "", icon: "ChevronUp", amount: "3 310 869", isProfit: true},
        {payMethod: "Приход", name: "", amount: "0"},
        {payMethod: "Безналичные", name: "", amount: "0"},
      ], 
      salesDataTwo: [
      {header: "Финансы до", dates: "15.02.2023-21.06.2023"},
        {payMethod: "Наличные", name: "", icon: "ChevronUp", amount: "369 383", isProfit: true},
        {payMethod: "Kaspi", name: "Акылжан", icon: "ChevronUp", amount: "546 596", isProfit: true},
        {payMethod: "Kaspi", name: "Адылжан", icon: "ChevronUp", amount: "770 092", isProfit: true},
        {payMethod: "Kaspi", name: "Мейржан", icon: "ChevronUp", amount: "17 000", isProfit: true},
        {payMethod: "QR", name: "Diler-kz", icon: "ChevronUp", amount: "154 200", isProfit: true},
        {payMethod: "QR", name: "Qastek", icon: "ChevronUp", amount: "339 850", isProfit: true},
        {payMethod: "QR", name: "Sherkhan", icon: "ChevronUp", amount: "888 008", isProfit: true},
        {payMethod: "Безналичные", name: "", icon: "ChevronUp", amount: "1 500", isProfit: false},
        {payMethod: "Безналичные", name: "", icon: "ChevronUp", amount: "227 240", isProfit: true},
        {payMethod: "Итого", name: "", icon: "ChevronUp", amount: "3 310 869", isProfit: true},
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/content.css");
</style>