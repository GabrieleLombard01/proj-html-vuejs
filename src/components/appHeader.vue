<script>
import { data } from '../data/index.js';

export default {
    computed: {
        headerNav() {
            return data.HeaderNav[0];
        }
    }
};
</script>

<template>
    <div class="margin_contents d-flex justify-content-between align-items-center">
        <div class="col-3">
            <img class="w-50" src="../assets/img/dark-logo.png" alt="logo">
        </div>
        <div class="col-9">
            <ul>
                <li v-for="(item, index) in headerNav" :key="index">
                    <a class="c_purple" href="#"><strong>{{ item }}</strong></a>
                </li>
                <button id="cart_shopping"><i class="fa-solid fa-cart-shopping"></i></button>
                <li>
                    <i class="fa-regular fa-circle-user fa-lg me-1"></i>
                    <input class="ps-3" type="search" placeholder="Search...">
                    <button><i class="ps-2 fa-solid fa-magnifying-glass"></i></button>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
ul button {
    border: none;
    background-color: white;
}

#cart_shopping {
    position: relative;
    right: 15px;
}
</style>
