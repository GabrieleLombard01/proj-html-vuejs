<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle },
    computed: {
        titleThirdSection() {
            return data.titleThirdSection[0];
        },
    },
};
</script>

<template>
    <section>
        <div class="margin_contents">
            <appTitle :title="titleThirdSection" />
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: #f5f5f5;
    width: 100%;
    height: 80vh;
}
</style>