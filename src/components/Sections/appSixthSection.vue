<script>
import appTitle from '../appTitle.vue';
import cardRoles from '../Cards/appCardRoles.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle, cardRoles },
    computed: {
        titleSixthSection() {
            return data.titleSixthSection[0];
        },
    },
};
</script>

<template>
    <section>
        <div class="margin_contents">
            <appTitle class="text-center pt-5" :title="titleSixthSection" />
            <!-- CARDS: -->
            <cardRoles />

            <div class="margin_content mb-5">
                <!--PREVIEW DOTS:-->
                <div class="preview_dots text-center">
                    <i class="fa-solid fa-circle"></i>
                    <i class="fa-regular fa-circle"></i>
                    <i class="fa-regular fa-circle"></i>
                    <i class="fa-regular fa-circle"></i>
                </div>
                <!--START BUTTON:-->
                <div class="start_today text-center">
                    <h2 class="d-inline pe-2">Start today for getting</h2>
                    <a href="#">Online Certification</a>
                    <h1>You can be your own guiding star with our help!</h1>
                    <button class="main_btn mt-4">Get started now</button>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
section {
    background-color: #f8f8f8;
    width: 100%;
    min-height: 80vh;
}

h1 {
    font-weight: 800;
    font-size: 35px;
    color: #3f3a64;
}

h2 {
    font-weight: 600;
    font-size: 25px;
}

a {
    color: #20ad96;
    font-weight: 600;
    font-size: 25px;
}

i {
    padding-top: 35px;
    padding-left: 5px;
    padding-right: 5px;
}

.preview_dots {
    height: 100px;
    margin-bottom: 50px;
}
</style>