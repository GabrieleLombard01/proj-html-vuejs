<script>
import appTitle from '../appTitle.vue';
import cardRoles from '../Cards/appCardRoles.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle, cardRoles },
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
            <appTitle class="text-center pt-5" :title="titleSixthSection" />
            <!-- CARDS: -->
            <cardRoles />
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: #f8f8f8;
    width: 100%;
    min-height: 80vh;
}
</style>