<template>
  <div class="menu-container">
    <div class="menu-container-header" v-if="menuHeader !== ''">
      <span>{{ menuHeader }}</span>
    </div>

    <MenuElement v-for="(item, index) in menuItems" :key="index"
      :menuText="item.text" :icon="item.icon" :showRightIcon="item.showRightIcon" :rightIcon="'Badge'"/>
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
    menuItems: Array,
    dropdownIcon: String,
  } 
}
</script>