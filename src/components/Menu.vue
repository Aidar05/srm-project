<template>
  <div id="left-menu">
    <div id="logo-container">
      <Icon :name="'Logo'"/>

      <span id="logo-text">AlloMaster</span>
    </div>

    <DashboardContainer />

    <MenuContainer menuHeader="Основное" :menuItems="[
        {text: 'Главная', icon: 'HomeTwo'},
        {text: 'Сервис', icon: 'Tool'},
        {text: 'Магазин', icon:'ShoppingCart'},
        {text: 'Задачи', icon: 'ListDetails'},
        {text: 'Записи', icon: 'ListCheck'},
        {text: 'Финансы', icon: 'FileDollar'},
        {text: 'Склад', icon: 'BuildingWarehouse'},
        {text: 'Заказы', icon: 'Package'}
      ]"/>

    <MenuContainer menuHeader="Справочники" :menuItems="[
        {text: 'Клиенты', icon: 'Users'},
        {text: 'Устройства', icon: 'ColorSwatch'},
        {text: 'Товары', icon:'Box'},
        {text: 'Услуги', icon: 'LayoutTwo'},
        {text: 'Другое', icon: 'MenuTwo'}
      ]"/> 

    <MenuContainer menuHeader="Отчеты" :menuItems="[
        {text: 'Должники', icon: 'UserMinus'},
        {text: 'Кредиторы', icon: 'UserPlus'},
        {text: 'Движение товара', icon:'Replace'},
        {text: 'Расход товара', icon: 'TransferOut'},
        {text: 'По продажам', icon: 'FileDollar'},
        {text: 'По сервису', icon: 'FileAnalytics'},
        {text: 'По сотрудникам', icon: 'User'},
      ]"/>

    <MenuContainer menuHeader="Параметры" :menuItems="[
        {text: 'Настройки', icon: 'Settings'},
        {text: 'База данных', icon: 'Database'},
        {text: 'SQL commands', icon:'BrandTabler'}
      ]"/>
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
}
}
</script>

<style>
@import url("../assets/css/menu.css");

</style>