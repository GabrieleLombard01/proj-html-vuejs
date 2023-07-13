<script>
import { data } from '../data/index.js';

export default {
    data() {
        return {
            isCartVisible: false,
            headerNav: [],
        };
    },
    mounted() {
        this.headerNav = data.HeaderNav[0];
    },
    methods: {
        toggleCart() {
            this.isCartVisible = !this.isCartVisible;
        },
    },
};
</script>

<template>
    <div class="margin_header_contents d-flex justify-content-between align-items-center">
        <div class="col-3">
            <img class="w-50" src="../assets/img/dark-logo.png" alt="logo">
        </div>
        <div class="col-9 position-relative">
            <ul>
                <li v-for="(item, index) in headerNav" :key="index">
                    <a class="c_purple" href="#"><strong>{{ item }}</strong></a>
                </li>
                <button id="cart_shopping" @click="toggleCart">
                    <i class="fa-solid fa-cart-shopping"></i>
                </button>
                <li>
                    <i class="fa-regular fa-circle-user fa-lg me-1"></i>
                    <input class="ps-3" type="search" placeholder="Search...">
                    <button id="searchBtn"><i class="ps-2 fa-solid fa-magnifying-glass"></i></button>
                </li>
            </ul>
            <div class="cart_container" :style="{ display: isCartVisible ? 'block' : 'none' }">
                <div class="row">
                    <div class="col-6">
                        <img src="../assets/img/shopping-cart_icon.png">
                    </div>
                    <div class="col-6 p-2">
                        <h2>
                            Oops... It looks like your cart is empty
                        </h2>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
h2 {
    font-size: 24px;
}

ul button {
    border: none;
    background-color: white;
}

li a:hover {
    text-decoration: underline;
    color: #20ad96;
}

input {
    height: 45px;
    width: 70%;
    border-style: none;
    border-top-left-radius: 8px;
    border-bottom-left-radius: 8px;
    background-color: #f5f5f5;
}

#searchBtn {
    background-color: #f5f5f5;
    height: 45px;
    border-top-right-radius: 8px;
    border-bottom-right-radius: 8px;
}

#cart_shopping {
    position: relative;
    right: 15px;
    color: #3f3a64;
}

.fa-magnifying-glass {
    padding-right: 20px;
    color: #20ad96;
    border-top-right-radius: 8px;
    border-bottom-right-radius: 8px;
}

.fa-circle-user:hover {
    cursor: pointer;
    color: #20ad96;
}

.fa-cart-shopping:hover {
    color: #20ad96;
    cursor: pointer;
}

.cart_container {
    min-height: 100px;
    width: 400px;
    border-radius: 10px;
    background-color: #f5f5f5;
    box-shadow: 1px 1px 8px 3px;
    position: absolute;
    top: 65%;
    left: 65%;
    display: none;
    padding: 10px;
}

.cart_container .col-6 img {
    width: 150px;
}
</style>



