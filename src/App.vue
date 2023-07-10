<script >
import demoSelect from './components/appDemoSelect.vue';

export default {
  components: { demoSelect },
};
</script>

<template>
  <div class="layout_container">

    <!-- MAIN-CONTAINER: -->
    <div class="left_container">

      <!-- header: -->
      <header>
        <div class="margin_contents d-flex justify-content-between align-items-center ps-3 pe-3">
          <div class="col-4">
            <img src="../src/assets/img/dark-logo.png" alt="logo">
          </div>
          <div class="col-4">
            <ul>
              <li><a href="#">link</a></li>
              <li><a href="#">link</a></li>
              <li><a href="#">link</a></li>
              <li><a href="#">link</a></li>
            </ul>
          </div>
        </div>
      </header>
    </div>

    <!-- DEMOSELECT-CONTAINER: -->
    <demoSelect />
  </div>
</template>

<style lang="scss">
@use './assets/scss/style.scss'
</style>
