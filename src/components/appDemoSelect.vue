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
    <div class="right_container" :class="{ 'right_container_after_click': isClicked }"></div>
    <div class="demoSelect_container" :style="{ 'margin-right': isClicked ? '20%' : '0' }">
        <button class="d-block p-2 pe-3" @click="handleClick">
            <i class="fa-solid fa-ruler-combined fa-lg"></i>
        </button>
        <button class="d-block p-2">
            <a href="https://thememove.ticksy.com/">
                <i class="fa-regular fa-futbol fa-lg"></i>
            </a>
        </button>
        <button class="d-block p-2">
            <a href="https://document.thememove.com/maxcoach/">
                <i class="fa-solid fa-book fa-lg"></i>
            </a>
        </button>
        <button class="d-block p-2">
            <a href="https://themeforest.net/item/maxcoach-online-courses-education-wp-theme/26051639">
                <i class="fa-solid fa-cart-shopping fa-lg"></i>
            </a>
        </button>
    </div>
</template>


<style scoped>
.right_container {
    width: 20%;
    min-height: 100vh;
    background-color: beige;
    position: absolute;
    right: 0;
    top: 0;
    bottom: 0;
    display: none;
    z-index: 2;
}

.right_container_after_click {
    display: block;

}

/* BUTTON */
.demoSelect_container {
    position: fixed;
    top: 30%;
    right: 0;
    padding: 5px;
    box-shadow: 0.5px 1px 1px 1px rgb(184, 184, 184);
    background-color: white;
    border-radius: 5%;
}

.demoSelect_container button {
    border-style: none;
    width: 40px;
    background-color: white;
    color: #111111;
}

/* Pseudo-classes: */
.demoSelect_container button:active {
    background-color: rgb(224, 224, 224);
    border-radius: 10%;
}
</style>
  