<script>
import { store } from '../data/store.js';

export default {

};
</script>

<template>
    <div class="jumbo">
        <!--TEXT:-->
        <div class="text_jumbo_container w-50">
            <div class="text_jumbo">
                <h1></h1>
                <p></p>
            </div>
        </div>
        <!--IMG:-->
        <figure class="w-50">
            <img src="" alt="">
        </figure>

    </div>
</template>

<style scoped>
.jumbo {
    height: 80vh;
    width: 100%;
    background-color: #e9e6e3;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 200px;
}

.text_jumbo {
    width: 420px;
    border: dashed black 1px;
}
</style>