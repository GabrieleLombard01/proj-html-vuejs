<script>
import appTitle from '../appTitle.vue';
import appCardFeature from '../Cards/appCardFeature.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle, appCardFeature },
    computed: {
        titleThirdSection() {
            return data.titleThirdSection[0];
        },
    },
};
</script>

<template>
    <section>
        <div class="margin_contents pt-5 mt-5 pb-5 mb-5">
            <appTitle class="text-center" :title="titleThirdSection" />
            <appCardFeature />
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: #f5f5f5;
    width: 100%;
    min-height: 80vh;
}
</style>