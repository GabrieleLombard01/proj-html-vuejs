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
    <section class="bg_data pt-5">
        <!--CONTENT:-->
        <div class="margin_contents row">
            <div class="col-6 pt-5">
                <img class="pt-4" src="../../assets/img/about-us-03-image-01.png" alt="about-us">
            </div>
            <div class="col-6 ">
                <div class="title_container">
                    <appTitle :title="titleSecondSection" />
                </div>

                <div class="career_container">
                    <div class="row align-items-center">
                        <div class="col-11">{{ careerCont.firstBlock }}</div>
                        <div class="col-1"><i class="fa-solid fa-plus"></i></div>
                    </div>
                </div>

                <div class="career_contained">
                    {{ careerCont.firstInsideBlock }}
                </div>

                <div class="career_container">
                    <div class="row align-items-center">
                        <div class="col-11">{{ careerCont.secondBlock }}</div>
                        <div class="col-1"><i class="fa-solid fa-plus"></i></div>
                    </div>
                </div>



                <div class="career_container">
                    <div class="row align-items-center">
                        <div class="col-11">{{ careerCont.thirdBlock }}</div>
                        <div class="col-1"><i class="fa-solid fa-plus"></i></div>
                    </div>
                </div>



                <!--accordion:-->

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
/* accordion */




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
    margin: 20px 20px 0px 0;
    width: 85%;
    height: 60px;
    border-radius: 10px;
    padding: 16px;
    border: solid grey 1px;
    background-color: #62c5b5;
    color: white;
    font-weight: 700;
}

.career_contained {
    margin: 0px 20px 20px 0px;
    width: 85%;
    min-height: 60px;
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
    padding: 16px;
    box-sizing: 1px 1px 8px 3px grey;
    background-color: #ffffff;
    color: rgb(105, 105, 105);
    font-weight: 500;
}

.fa-plus {
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

.bg_data {
    background-color: #faf8f6;
}
</style>