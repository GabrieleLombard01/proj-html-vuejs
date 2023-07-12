<script>
export default {
    props: ['title'],
};
</script>

<template>
    <div>
        <h5>{{ title.surtitle }}</h5>
        <h2>{{ title.title }}</h2>
    </div>
</template>

<style>
h2 {
    font-weight: 800;
    color: #3f3a64;
}

h5 {
    color: grey;
    font-size: 17px;
}
</style>