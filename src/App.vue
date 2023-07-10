<script >
import demoSelect from './components/appDemoSelect.vue';
import appHeader from './components/appHeader.vue';
import jumbo from './components/jumbo.vue';

export default {
  components: { demoSelect, appHeader, jumbo },
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

      <!-- main-content: -->
      <main class="margin_contents bg-light">

        <!-- JUMBO: -->
        <jumbo />

      </main>


    </div>

    <!-- DEMOSELECT-CONTAINER: -->
    <demoSelect />
  </div>
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
