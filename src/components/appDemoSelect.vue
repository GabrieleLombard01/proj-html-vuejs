<script>
import appMaxcoach from './appMaxcoach.vue';
import appGrid from './appGrid.vue';
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
    components: { appMaxcoach, appGrid },
};
</script>

<template>
    <div class="right_container" :class="{ 'right_container_after_click': isClicked }">
        <!--TEXT-->
        <appMaxcoach />
        <!--row:-->
        <appGrid />
    </div>
    <div class="demoSelect_container" :style="{ 'margin-right': isClicked ? '20%' : '0' }">
        <button class="d-block p-2 pe-3" @click="handleClick">
            <i class="fa-solid fa-ruler-combined fa-lg"></i>
        </button>
        <div class="tooltip" v-if="showTooltip">Select Demo</div>


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
    <div class="suggestion "><span>Select Demo</span></div>
</template>


<style scoped>
.suggestion {
    height: 40px;
    min-width: 100px;
    background-color: rgba(0, 0, 0, 0.9);
    border-radius: 15px;
    position: absolute;
    top: 30%;
    right: 3%;
    color: white;
    font-weight: 700;
    padding-left: 5px;
    padding-right: 5px;
    padding-top: 7px;
    display: none;
}

.fa-ruler-combined:hover.suggestion {
    display: block;
}

.right_container {
    box-shadow: 2px 2px 8px 1px rgb(99, 99, 99);
    width: 20%;
    min-height: 100vh;
    background-color: white;
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

.tooltip {
    position: absolute;
    background-color: yellow;
    color: black;
    padding: 5px;
    left: -80px;
    top: 0;
}

/* Pseudo-classes: */
.demoSelect_container button:active {
    background-color: rgb(224, 224, 224);
    border-radius: 10%;
}
</style>
  