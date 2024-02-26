<template>
  <div class="menu-container" id="dashboard">
    <div class="menu-container-header">
      <span>{{ menuHeader }}</span>
    </div>

    <MenuElement v-for="(item, index) in menuItems" :key="index"
      :menu_text="item.text" :icon="item.icon"/>
  </div>
</template>

<script>
import MenuElement from './MenuElement.vue';
import Icon from './Icon.vue';

export default{
  name: "MenuContainer",
  components: {
    MenuElement, Icon
  },
  props: {
    menuHeader: String,
    menuItems: Array
  }
}
</script>