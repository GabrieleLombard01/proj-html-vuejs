<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle },
    computed: {
        titleSecondSection() {
            return data.titleSecondSection[0];
        },
    },
};
</script>

<template>
    <section>
        <div class="margin_contents">
            <appTitle :title="titleSecondSection" />
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: white(191, 191, 191);
    width: 100%;
    height: 80vh;
}
</style>