<script>
import appTitle from '../appTitle.vue';
import cardLearn from '../Cards/appCardLearn.vue';
import { data } from '../../data/index';


export default {
    components: { appTitle, cardLearn },
    computed: {
        titleFirstSection() {
            return data.titleFirstSection[0];
        },
    },
};
</script>

<template>
    <section>
        <div class="margin_contents text-center pt-5">
            <appTitle :title="titleFirstSection" />

            <!-- CARDS: -->
            <cardLearn />

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