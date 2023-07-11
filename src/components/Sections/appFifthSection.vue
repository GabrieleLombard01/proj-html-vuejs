<script>
import appTitle from '../appTitle.vue';
import cardEvents from '../Cards/appCardEvents.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle, cardEvents },
    computed: {
        titleFifthSection() {
            return data.titleFifthSection[0];
        },
    },
};
</script>

<template>
    <section class="mt-5">
        <div class="margin_contents">
            <appTitle class="text-center" :title="titleFifthSection" />
            <!-- CARDS: -->
            <cardEvents />
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: white;
    width: 100%;
    min-height: 80vh;
}
</style>