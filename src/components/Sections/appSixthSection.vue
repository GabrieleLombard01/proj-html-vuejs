<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle },
    computed: {
        titleSixthSection() {
            return data.titleSixthSection[0];
        },
    },
};
</script>

<template>
    <section>
        <div class="margin_contents">
            <appTitle :title="titleSixthSection" />
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: #f8f8f8;
    width: 100%;
    height: 80vh;
}
</style>