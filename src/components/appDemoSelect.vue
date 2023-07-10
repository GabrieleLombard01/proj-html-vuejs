<script>
export default {
    data() {
        return {
            isClicked: false,
        };
    },
    methods: {
        handleClick() {
            this.isClicked = !this.isClicked;
        },
    },
};
</script>

<template>
    <div class="right_container" :class="{ 'right_container_after_click': isClicked }">ciao</div>
    <button @click="handleClick">vai</button>
</template>

<style scoped>
.right_container {
    width: 30%;
    height: 500px;
    background-color: beige;
    position: absolute;
    right: 0;
    top: 0;
    bottom: 0;
    display: none;
}

.right_container_after_click {
    display: block;
}
</style>
  