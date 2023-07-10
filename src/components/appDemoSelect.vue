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
    <div class="demoSelect_container" :style="{ 'margin-right': isClicked ? '20%' : '0' }">
        <button class="bg-success d-block p-2 pe-3" @click="handleClick">vai</button>
        <button class="d-block p-2">link</button>
        <button class="d-block p-2">link</button>

    </div>
</template>


<style scoped>
.right_container {
    width: 20%;
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

/* BUTTON */
.demoSelect_container {
    position: fixed;
    top: 30%;
    right: 0;

}
</style>
  