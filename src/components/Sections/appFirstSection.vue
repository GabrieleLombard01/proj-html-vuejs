<script>
import appTitle from '../appTitle.vue'
export default {
    components: { appTitle },
    computed: {

    },

};
</script>

<template>
    <section>
        <div class="margin_contents">
            <appTitle />
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