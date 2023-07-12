<script>
import { data } from '../data/index.js';

export default {
    computed: {
        headerNav() {
            return data.HeaderNav[0];
        },
    },
    data() {
        return {
            hoveredIndex: null
        };
    },
    methods: {
        showDiv(index) {
            this.hoveredIndex = index;
        },
        hideDiv(index) {
            this.hoveredIndex = null;
        },
        isHovered(index) {
            return this.hoveredIndex === index;
        }
    }
};
</script>

<template>
    <div class="margin_header_contents d-flex justify-content-between align-items-center">
        <div class="col-3">
            <img class="w-50" src="../assets/img/dark-logo.png" alt="logo">
        </div>
        <div class="col-9">
            <ul>
                <li v-for="(item, index) in headerNav" :key="index" @mouseover="showDiv(index)"
                    @mouseleave="hideDiv(index)">
                    <a class="c_purple" href="#"><strong>{{ item }}</strong></a>
                    <div v-if="isHovered(index)" class="show_container row">
                        <ul>
                            <li>Click to learn more</li>
                        </ul>
                    </div>
                </li>
                <button id="cart_shopping"><i class="fa-solid fa-cart-shopping"></i></button>
                <li>
                    <i class="fa-regular fa-circle-user fa-lg me-1"></i>
                    <input class="ps-3" type="search" placeholder="Search...">
                    <button id="searchBtn"><i class="ps-2 fa-solid fa-magnifying-glass"></i></button>
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

input:focus {
    border-style: none;
    border: #f5f5f5;
}

#cart_shopping {
    position: relative;
    right: 15px;
}

#searchBtn {
    background-color: #f5f5f5;
    height: 45px;
    border-top-right-radius: 8px;
    border-bottom-right-radius: 8px;
}

.show_container {
    position: absolute;
    box-shadow: 2px 2px 10px 2px rgb(123, 123, 123);
    min-height: 5px;
    padding-bottom: 15px;
    border-bottom: solid #20ad96 3px;
    background-color: white;
    border-radius: 8px;
    line-height: 35px;
    cursor: pointer;
    font-weight: 600;
    color: grey;
}

.show_container li:hover {
    color: #20ad96;
    text-decoration: underline;
}

.fa-magnifying-glass {
    padding-right: 20px;
    color: #20ad96;
    border-top-right-radius: 8px;
    border-bottom-right-radius: 8px;
}

.fa-circle-user {
    cursor: pointer;
}
</style>



