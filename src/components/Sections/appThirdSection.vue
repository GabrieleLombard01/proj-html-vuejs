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
        <div class="margin_contents pt-5 mt-5 pb-5">
            <appTitle class="text-center" :title="titleThirdSection" />
            <appCardFeature />
        </div>
    </section>
    <div class="bg_curv">
    </div>
</template>

<style scoped>
section {
    background-image: linear-gradient(to bottom, white, #f6f6f6, #ececec);
    background-color: #f5f5f5;
    width: 100%;
    min-height: 80vh;
}

.bg_curv {
    height: 50px;
    width: 100%;
    background-image: url(../../assets/img/curved.png);
    background-size: cover;
}
</style>