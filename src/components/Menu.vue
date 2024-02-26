<template>
  <div id="left-menu">
    <div id="logo-container">
      <Icon :name="'Logo'"/>

      <span id="logo-text">AlloMaster</span>
    </div>

    <MenuContainer menuHeader="" :menuItems="dashboardContainer" :dropdownIcon="'ChevronDown'"/>      

    <MenuContainer menuHeader="Основное" :menuItems="mainContainer"/>      

    <MenuContainer menuHeader="Справочники" :menuItems="referencesContainer"/> 

    <MenuContainer menuHeader="Отчеты" :menuItems="reportsContainer"/>

    <MenuContainer menuHeader="Параметры" :menuItems="settingsContainer"/>
  </div>

</template>

<script>
import DashboardContainer from './MenuComponents/DashboardContainer.vue';
import Icon from './MenuComponents/Icon.vue';
import MenuContainer from './MenuComponents/MenuContainer.vue';

export default{
  name: "Menu",
  components: {
    DashboardContainer, MenuContainer,
    Icon
  },
  data() {
    return{
      mainContainer: [
        {text: 'Главная', icon: 'HomeTwo', showRightIcon: false},
        {text: 'Сервис', icon: 'Tool', showRightIcon: false},
        {text: 'Магазин', icon:'ShoppingCart', showRightIcon: false},
        {text: 'Задачи', icon: 'ListDetails', showRightIcon: true},
        {text: 'Записи', icon: 'ListCheck', showRightIcon: true},
        {text: 'Финансы', icon: 'FileDollar', showRightIcon: false},
        {text: 'Склад', icon: 'BuildingWarehouse', showRightIcon: false},
        {text: 'Заказы', icon: 'Package', showRightIcon: true}
      ], 
      referencesContainer: [
        {text: 'Клиенты', icon: 'Users', showRightIcon: false},
        {text: 'Устройства', icon: 'ColorSwatch', showRightIcon: false},
        {text: 'Товары', icon:'Box', showRightIcon: false},
        {text: 'Услуги', icon: 'LayoutTwo', showRightIcon: true},
        {text: 'Другое', icon: 'MenuTwo', showRightIcon: false}
      ],
      reportsContainer: [
        {text: 'Должники', icon: 'UserMinus', showRightIcon: false},
        {text: 'Кредиторы', icon: 'UserPlus', showRightIcon: true},
        {text: 'Движение товара', icon:'Replace', showRightIcon: false},
        {text: 'Расход товара', icon: 'TransferOut', showRightIcon: false},
        {text: 'По продажам', icon: 'FileDollar', showRightIcon: true},
        {text: 'По сервису', icon: 'FileAnalytics', showRightIcon: false},
        {text: 'По сотрудникам', icon: 'User', showRightIcon: false},
      ], 
      settingsContainer: [
        {text: 'Настройки', icon: 'Settings', showRightIcon: false },
        {text: 'База данных', icon: 'Database', showRightIcon: false},
        {text: 'SQL commands', icon:'BrandTabler', showRightIcon: false}
      ],
      dashboardContainer: [
      {text: 'Добавить', icon: 'CirclePlus', showRightIcon: true},
      {text: 'Новый ремонт', icon: 'Point', showRightIcon: false},
      {text: 'Новая продажа', icon:'Point', showRightIcon: false}
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/menu.css");

</style>