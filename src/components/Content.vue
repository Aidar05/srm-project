<template>
  <div class="content-main-container">

    <ContentBtns :contentIcons="contentIcons"/>
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
  data() {
    return {
      contentIcons: [
        {icon: "Repeat"},
        {icon: "CirclePlus"},
        {icon: "List"}
      ]
    }
  }
}
</script>

<style>
@import url("../assets/css/content.css");
</style>