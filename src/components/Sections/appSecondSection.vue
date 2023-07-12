<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle },
    computed: {
        titleSecondSection() {
            return data.titleSecondSection[0];
        },
        careerCont() {
            return data.careerCont[0];
        }
    },
};
</script>

<template>
    <section>
        <!--CONTENT:-->
        <div class="margin_contents row">
            <div class="col-6">
                <img src="../../assets/img/about-us-03-image-01.png" alt="about-us">
            </div>
            <div class="col-6 ">
                <div class="title_container">
                    <appTitle :title="titleSecondSection" />
                </div>
                <div class="career_container">{{ careerCont.firstBlock }}</div>
                <div class="career_container">{{ careerCont.secondBlock }}</div>
                <div class="career_container">{{ careerCont.thirdBlock }}</div>
            </div>
        </div>
        <!--DATA:-->
        <div class="data_lessions mt-5">
            <div class="col-3 text-center">
                <h1>{{ careerCont.numberSession }}</h1>
                <span>{{ careerCont.descrSession }}</span>
            </div>
            <div class="col-3 text-center">
                <h1>{{ careerCont.numberLearn }}</h1>
                <span>{{ careerCont.descrLearn }}</span>
            </div>
            <div class="col-3 text-center">
                <h1>{{ careerCont.numberInstr }}</h1>
                <span>{{ careerCont.descrInstr }}</span>
            </div>
            <div class="col-3 text-center">
                <h1>{{ careerCont.numberRate }}</h1>
                <span>{{ careerCont.descrRate }}</span>
            </div>

        </div>
    </section>
</template>

<style scoped>
section {
    background-color: #fefefe;
    width: 100%;
    height: 80vh;
}

/* Utilties */
.title_container {
    width: 60%;
}

.career_container {
    margin: 20px 20px 20px 0;
    width: 85%;
    height: 60px;
    border-radius: 10px;
    padding: 20px;
    border: solid grey 1px;
}

/* DATA LESSIONS: */
.data_lessions {
    margin: auto;
    width: 1400px;
    height: 150px;
    background-color: #faf8f6;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
</style>