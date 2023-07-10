<script >
import demoSelect from './components/appDemoSelect.vue';
import appHeader from './components/appHeader.vue';

export default {
  components: { demoSelect, appHeader },
};
</script>

<template>
  <div class="layout_container">

    <!-- MAIN-CONTAINER: -->
    <div class="left_container">

      <!-- header: -->
      <header>
        <appHeader />
      </header>
    </div>

    <!-- DEMOSELECT-CONTAINER: -->
    <demoSelect />
  </div>
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
