<template>
  <div class="content-main-container">
    <ContentBtns :icon="'CirclePlus'"/>
  </div>
</template>

<script>
import Icon from './MenuComponents/Icon.vue';
import ContentBtns from "./ContentComponents/ContentBtns.vue"

export default{
  name: "Content",
  components: {
    Icon, ContentBtns
  },
}
</script>

<style>
@import url("../assets/css/content.css");
</style>