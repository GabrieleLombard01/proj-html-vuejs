<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index';


export default {
    components: { appTitle },
    computed: {
        titleFirstSection() {
            return data.titleFirstSection[0];
        },
    },
};
</script>
  

<template>
    <section>
        <div class="margin_contents">
            <appTitle :title="titleFirstSection" />
        </div>
    </section>
</template>
  

<style scoped>
section {
    background-color: white;
    width: 100%;
    height: 80vh;
}
</style>
  