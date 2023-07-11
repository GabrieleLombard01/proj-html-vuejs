<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index.js';

export default {
    data() {
        return {
            tasks: [
                ...data.fourthCont,
            ],
            defaultPath: "../../src/assets/img/",
        };
    },
    components: { appTitle },
    computed: {
        titleFourthSection() {
            return data.titleFourthSection[0];
        },
        fourthContInf() {
            return data.fourthContInf[0];
        }
    },
};
</script>

<template>
    <!--FIRST SECTION-->
    <section class="mt-5">
        <div class="margin_contents mb-0">
            <div class="row justify-content-between">
                <div class="col-6">
                    <div class="text_container">
                        <appTitle :title="titleFourthSection" />
                    </div>
                    <ul>
                        <li v-for="task in tasks[0]" :key="task.firstTask">{{ task }}</li>
                    </ul>
                    <button class="main_btn mx-auto">Get started for free</button>
                </div>
                <div class="col-5">
                    <img class="" src="../../assets/img/home-5-image-01.png" alt="">
                </div>
            </div>
            <!--SECOND SECTION-->


            <div class="row justify-content-between">
                <div class="col-5">
                    <img class="" src="../../assets/img/home-5-image-02.png">
                </div>
                <div class="col-6">
                    <div class="text_container">
                        <h1>{{ fourthContInf.title }}</h1>
                    </div>
                    <p>{{ fourthContInf.descr }}</p>


                    <button class="main_btn mx-auto">Get started for free</button>
                </div>
            </div>
        </div>

    </section>
</template>
  

<style scoped>
section {
    background-color: white;
    width: 100%;
    min-height: 80vh;
}

ul {
    height: 50%;
    width: 60%;
    line-height: 40px;
}

.text_container {
    width: 45%;
    list-style: none;
}
</style>