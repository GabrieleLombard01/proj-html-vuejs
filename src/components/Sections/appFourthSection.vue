<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle },
    computed: {
        titleFourthSection() {
            return data.titleFourthSection[0];
        },
    },
};
</script>

<template>
    <section>
        <div class="margin_contents">
            <appTitle :title="titleFourthSection" />
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