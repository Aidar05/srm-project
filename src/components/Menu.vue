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
import Icon from './MenuComponents/Icon.vue';
import MenuContainer from './MenuComponents/MenuContainer.vue';

export default{
  name: "Menu",
  components: {
    MenuContainer, Icon
  },
  data() {
    return{
      dashboardContainer: [
        {text: 'Добавить', icon: 'CirclePlus', showRightIcon: true, isActive: false},
        {text: 'Новый ремонт', icon: 'Point', showRightIcon: false, isActive: true},
        {text: 'Новая продажа', icon:'Point', showRightIcon: false, isActive: false}
      ],
      mainContainer: [
        {text: 'Главная', icon: 'HomeTwo', showRightIcon: false, isActive: false},
        {text: 'Сервис', icon: 'Tool', showRightIcon: false, isActive: false},
        {text: 'Магазин', icon:'ShoppingCart', showRightIcon: false, isActive: false},
        {text: 'Задачи', icon: 'ListDetails', showRightIcon: true, isActive: false},
        {text: 'Записи', icon: 'ListCheck', showRightIcon: true, isActive: false},
        {text: 'Финансы', icon: 'FileDollar', showRightIcon: false, isActive: false},
        {text: 'Склад', icon: 'BuildingWarehouse', showRightIcon: false, isActive: false},
        {text: 'Заказы', icon: 'Package', showRightIcon: true, isActive: false}
      ], 
      referencesContainer: [
        {text: 'Клиенты', icon: 'Users', showRightIcon: false, isActive: false},
        {text: 'Устройства', icon: 'ColorSwatch', showRightIcon: false, isActive: false},
        {text: 'Товары', icon:'Box', showRightIcon: false, isActive: false},
        {text: 'Услуги', icon: 'LayoutTwo', showRightIcon: true, isActive: false},
        {text: 'Другое', icon: 'MenuTwo', showRightIcon: false, isActive: false}
      ],
      reportsContainer: [
        {text: 'Должники', icon: 'UserMinus', showRightIcon: false, isActive: false},
        {text: 'Кредиторы', icon: 'UserPlus', showRightIcon: true, isActive: false},
        {text: 'Движение товара', icon:'Replace', showRightIcon: false, isActive: false},
        {text: 'Расход товара', icon: 'TransferOut', showRightIcon: false, isActive: false},
        {text: 'По продажам', icon: 'FileDollar', showRightIcon: true, isActive: false},
        {text: 'По сервису', icon: 'FileAnalytics', showRightIcon: false, isActive: false},
        {text: 'По сотрудникам', icon: 'User', showRightIcon: false, isActive: false},
      ], 
      settingsContainer: [
        {text: 'Настройки', icon: 'Settings', showRightIcon: false, isActive: false},
        {text: 'База данных', icon: 'Database', showRightIcon: false, isActive: false},
        {text: 'SQL commands', icon:'BrandTabler', showRightIcon: false, isActive: false}
      ]
    } 
  }
}
</script>

<style>
@import url("../assets/css/menu.css");

</style>