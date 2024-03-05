<template>
  <div class="content-btns-container" :class="{ 'btn-group': hasText }">
    <div class="content-btns" v-for="(item, index) in contentIcons" 
      :key="index" >

      <Icon v-if="item.icon" :name="item.icon"/>
      <span v-else>{{ item.text }}</span> 
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
  },
  computed: {
    hasText() {
      return this.contentIcons.some(item => item.text);
    }
  }
}
</script>

<style>
@import url("../../assets/css/content.css");
</style>