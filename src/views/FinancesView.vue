<template>
  <Menu />

  <Header />

  <Content />
</template>

<script>
import Icon from "@/components/MenuComponents/Icon.vue";
import Menu from "../components/Menu.vue"
import Header from "@/components/Header.vue";
import Content from "@/components/Content.vue";

export default{
  name: "FinancesView",
  components: {
    Menu, Icon, Header, Content
}
}
</script>

<style>
@import url("../assets/css/header.css");
</style>