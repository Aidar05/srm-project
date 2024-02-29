<template>
  <Menu />

  <Header />
</template>

<script>
import Menu from "../components/Menu.vue"
import Header from "@/components/Header.vue";
import Icon from "@/components/MenuComponents/Icon.vue";

export default{
  name: "FinancesView",
  components: {
    Menu, Icon, Header
}
}
</script>

<style>
@import url("../assets/css/header.css");
</style>