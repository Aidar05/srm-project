<template>
  <div class="menu-element">  
    <Icon class="menu-left-icon" :name="icon" />

    <span class="menu-element-text">{{ menuText }}</span>

    <Icon class="menu-right-icon" :name="rightIcon" v-if="showRightIcon"/>
  </div>

</template>

<script>
import Icon from './Icon.vue';

export default {
  name: "MenuElement",
  components: {
    Icon
  },
  props: {
    menuText: String,
    icon: String,
    rightIcon: String,
    showRightIcon: Boolean,
  }
}
</script>

<style>
@import url("../../assets/css/menu.css");

</style>