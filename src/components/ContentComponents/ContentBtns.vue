<template>
  <div class="content-btns-container">
    <div class="content-btns" v-for="(item, index) in contentIcons" 
      :key="index" >

      <Icon :name="item.icon"/> 
    </div>
  </div>
</template>

<script>
import Icon from '../MenuComponents/Icon.vue';

export default{
  name: "Content",
  components: {
    Icon
  },
  props: {
    contentIcons: Object
  }
}
</script>

<style>
@import url("../../assets/css/content.css");
</style>