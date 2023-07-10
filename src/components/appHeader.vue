<script>
import { store } from '../data/store.js';

export default {
    computed: {
        headerNav() {
            return store.HeaderNav[0];
        }
    }
};
</script>

<template>
    <div class="margin_contents d-flex justify-content-between align-items-center ps-3">
        <div class="col-4">
            <img class="w-50" src="../assets/img/dark-logo.png" alt="logo">
        </div>
        <div class="col-8">
            <ul>
                <li v-for="(item, index) in headerNav" :key="index">
                    <a class="c_purple" href="#"><strong>{{ item }}</strong></a>
                </li>
            </ul>
        </div>
    </div>
</template>




