<script >
import demoSelect from './components/appDemoSelect.vue';
import appHeader from './components/appHeader.vue';
import cardSection from './components/appCardSect.vue';

export default {
  components: { demoSelect, appHeader, cardSection },
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
        <cardSection />
      </main>


    </div>

    <!-- DEMOSELECT-CONTAINER: -->
    <demoSelect />
  </div>
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
