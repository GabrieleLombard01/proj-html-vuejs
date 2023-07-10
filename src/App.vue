<script >
import demoSelect from './components/appDemoSelect.vue';

export default {
  components: { demoSelect },
};
</script>

<template>
  <div class="layout_container">
    <div class="left_container"></div>
    <demoSelect />
  </div>
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
