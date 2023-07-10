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
        <div class=" margin_contents d-flex align-items-center justify-content-between">
            <!-- TEXT -->
            <div class="text_jumbo_container w-50">
                <div class="text_jumbo">
                    <h1>{{ JumboContent.title }}</h1>
                    <h3 class="pt-4">{{ JumboContent.descr }}</h3>
                    <!-- BTN -->
                    <button class="mt-4 main_btn">{{ JumboContent.btn }}</button>
                </div>
            </div>
            <!-- IMG -->
            <figure>
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
    </div>
</template>

<style scoped>
.jumbo {
    height: 80vh;
    width: 100%;
    background-color: #e9e6e3;
    padding-top: 50px;
}

.text_jumbo {
    width: 460px;
    padding: 20px 20px 20px 0;
    border: dashed black 1px;

}

.jumbo figure {
    width: 41%;
}
</style>