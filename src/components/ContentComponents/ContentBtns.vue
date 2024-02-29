<template>
  <div class="content-btns">
    <Icon :name="icon"/> 
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
    icon: String
  }
}
</script>

<style>
@import url("../../assets/css/content.css");
</style>