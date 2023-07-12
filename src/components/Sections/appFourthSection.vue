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
                        <appTitle class="ps-5" :title="titleFourthSection" />
                    </div>
                    <ul>
                        <li class="d-flex" v-for="task in tasks[0]" :key="task.firstTask">
                            <img class="img-fluid" src="../../assets/img/check.webp">
                            <span>{{ task }}</span>
                        </li>
                    </ul>
                    <button class="main_btn ms-5">Get started for free</button>
                </div>
                <div class="col-5">
                    <img src="../../assets/img/home-5-image-01.png">
                </div>
            </div>

            <!--SECOND SECTION-->
            <div class="row justify-content-between">
                <div class="col-5">
                    <img class="" src="../../assets/img/home-5-image-02.png">
                </div>
                <div class="col-6">
                    <div class="text_container mx-auto mt-5 pt-5">
                        <h5>{{ fourthContInf.surtitle }}</h5>
                        <h2>{{ fourthContInf.title }}</h2>
                        <p>{{ fourthContInf.descr }}</p>
                        <button class="main_btn mx-auto">Download our app</button>
                    </div>
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

button {
    font-weight: 700;
}

p {
    padding-top: 20px;
    padding-bottom: 30px;
    font-weight: 700;
    color: grey;
}

ul {
    height: 40%;
    width: 90%;

}

li {
    height: 50px;
    color: grey;
    font-weight: 700;
}

li img {
    height: 20px;
    padding-right: 10px;
}

.text_container {
    width: 65%;
}
</style>