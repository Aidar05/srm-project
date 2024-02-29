<template>
  <div class="nav-element" :class=" {activeNav: activeNav} ">
    <span class="nav-text"> {{ navText }} </span>
    
    <Icon :name="'X'"/>
  </div>
</template>

<script>
import Icon from '../MenuComponents/Icon.vue';

export default{
  name: "NavElement",
  components: {
    Icon
  },
  props: {
    navText: String,
    activeNav: Boolean,
  }
}
</script>