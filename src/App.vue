<script >
import demoSelect from './components/appDemoSelect.vue';
import appHeader from './components/appHeader.vue';
import jumbo from './components/jumbo.vue';
import firstSect from './components/Sections/appFirstSection.vue';
import secondSect from './components/Sections/appSecondSection.vue';
import thirdSect from './components/Sections/appThirdSection.vue';
import fourthSect from './components/Sections/appFourthSection.vue';
import fifthSect from './components/Sections/appFifthSection.vue';
import sixthSect from './components/Sections/appSixthSection.vue';
import appFooter from './components/appFooter.vue';

export default {
  components: { demoSelect, appHeader, jumbo, firstSect, secondSect, thirdSect, fourthSect, fifthSect, sixthSect, appFooter },
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
      <main>

        <!-- JUMBO: -->
        <jumbo />

        <!-- SECTIONS: -->
        <firstSect />

        <secondSect />

        <thirdSect />

        <fourthSect />

        <fifthSect />

        <sixthSect />

        <!-- FOOTER: -->
        <appFooter />

      </main>

    </div>

    <!-- DEMOSELECT-CONTAINER: -->
    <demoSelect />

  </div>
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
