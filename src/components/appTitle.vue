<script>
import { data } from '../data/index.js';
export default {
    computed: {
        titleFirstSection() {
            return data.titleFirstSection[0];
        }
    }
};
</script>

<template>
    <h5>{{ titleFirstSection.surtitle }}</h5>
    <h2>{{ titleFirstSection.title }}</h2>
</template>

<style></style>