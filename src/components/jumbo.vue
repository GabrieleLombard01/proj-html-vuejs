<script>
import { store } from '../data/store.js';

export default {
    computed: {
        JumboContent() {
            return store.JumboContent[0];
        }
    }
};
</script>

<template>
    <div class="jumbo">
        <!-- TEXT -->
        <div class="text_jumbo_container w-50">
            <div class="text_jumbo">
                <h1>{{ JumboContent.title }}</h1>
                <p>{{ JumboContent.descr }}</p>
            </div>
        </div>
        <!-- IMG -->
        <figure class="w-50">
            <img src="../assets/img/home-5-hero-image.png" :alt='JumboContent.title'>
            <!--
                Ho dovuto per forza fare così perchè 
                :src='JumboContent.img_uri' non
                funzionava, ho controllato in console
                e il percorso era corretto, ma non
                si vedeva comunque nulla in pagina
            -->
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
    width: 390px;
    padding: 20px 20px 20px 0;
    border: dashed black 1px;
}
</style>