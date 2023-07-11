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
    background-color: rgb(202, 10, 10);
    width: 100%;
    height: 80vh;
}
</style>