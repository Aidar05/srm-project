<template>
  <div class="menu-container">
    <span class="menu-headline"> {{ menu_headline }} </span>
  
    <div class="menu-elements">
      <div class="menu-element"></div>
    </div>
  </div>
</template>

<script>
export default{
  name: "MenuContainer",
  props: {
    menu_headline: String
  }
}
</script>