<template>
  <Menu />

  <Header />
</template>

<script>
import IndentDeacrease from "@/assets/icons/vue/IndentDeacrease.vue";
import Menu from "../components/Menu.vue"
import Icon from "@/components/MenuComponents/Icon.vue";
import Header from "@/components/Header.vue";

export default{
  name: "FinancesView",
  components: {
    Menu, Icon, Header
}
}
</script>

<style>
@import url("../assets/css/header.css")
</style>