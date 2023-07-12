<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle },
    data() {
        return {
            careerCont: data.careerCont.slice(0, 3).map((block) => ({
                ...block,
                opened: false,
            })),
        };
    },
    methods: {
        toggleAccordion(index) {
            this.careerCont[index].opened = !this.careerCont[index].opened;
        },
    },
    computed: {
        titleSecondSection() {
            return data.titleSecondSection[0];
        },
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
                <!--ACCORDION:-->
                <div class="career_container" v-for="(block, index) in careerCont" :key="index"
                    @click="toggleAccordion(index)">
                    <div class="row align-items-center">
                        <div class="col-11">{{ block.firstBlock }}</div>
                        <div class="col-1">
                            <i :class="{ 'fa-solid fa-plus': !block.opened, 'fa-solid fa-minus': block.opened }"></i>
                        </div>
                    </div>
                    <div v-if="block.opened" class="accordion_content">
                        <p>{{ block.firstInsideBlock }}</p>
                    </div>
                </div>






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
    min-height: 80vh;
}

h1 {
    color: #20ad96;
    font-weight: 900;
    padding-bottom: 15px;
}

span {
    font-weight: 700;
    font-size: 16px;
}

/* Utilties */
.title_container {
    width: 60%;
    margin-bottom: 50px;
}

.career_container {
    margin: 20px 20px 20px 0;
    width: 85%;
    height: 60px;
    border-radius: 10px;
    padding: 16px;
    border: solid grey 1px;
    background-color: #62c5b5;
    color: white;
    font-weight: 700;
}

.fa-plus {
    border: solid white 1px;
    padding: 5px;
    border-radius: 50%;
    cursor: pointer;
}

.fa-minus {
    border: solid white 1px;
    padding: 5px;
    border-radius: 50%;
    cursor: pointer;
}

.fa-plus:hover {
    color: #62c5b5;
    background-color: white;
}

.fa-minus:hover {
    color: #62c5b5;
    background-color: white;
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

/* ACCORDION: */
.accordion_content {
    padding: 16px;
    border: solid grey 1px;
    border-radius: 5px;
    background-color: white;
    color: #333;
    font-weight: 700;
}
</style>