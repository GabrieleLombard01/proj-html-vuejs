<script >
import demoSelect from './components/appDemoSelect.vue';
import appHeader from './components/appHeader.vue';
import jumbo from './components/jumbo.vue';
import firstSect from './components/Sections/appFirstSection.vue';

export default {
  components: { demoSelect, appHeader, jumbo, firstSect },
};
</script>

<template>
  <div class="container-fluid">

    <!-- MAIN-CONTAINER: -->
    <div class="left_container">

      <!-- header: -->
      <header>
        <appHeader />
      </header>

      <!-- main-content: -->
      <main class="ps-3">

        <!-- JUMBO: -->
        <jumbo />

        <!-- section: -->
        <firstSect />


        <p class="margin_contents ">

        </p>
      </main>

    </div>

    <!-- DEMOSELECT-CONTAINER: -->
    <demoSelect />

  </div>
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
