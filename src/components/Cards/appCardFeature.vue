<script>
import { data } from "../../data/index";

export default {
    data() {
        return {
            cards: [
                ...data.firstCardFeature,
                ...data.secondCardFeature,
                ...data.thirdCardFeature,
                ...data.fourthCardFeature,
                ...data.fifthCardFeature,
                ...data.sixthCardFeature,
            ],
            defaultPath: "../../src/assets/img/",
        };
    },
};
</script>

<template>
    <div class="row pb-3">
        <div class="col-4 pt-5" v-for="(card, index) in cards" :key="index">
            <div class="card">
                <img :src="defaultPath + card.srcImg">
                <div class="d-flex align-items-center">
                    <div class="col-2 ps-4 pt-3">
                        <img :src="defaultPath + card.userUri">
                    </div>
                    <div class="col-10 pt-3">
                        <span>{{ card.user }}</span>
                    </div>
                </div>
                <h3 class="card_title pt-2 ps-4">{{ card.title }}</h3>
            </div>
        </div>
        <button class="main_btn mx-auto w-25 mt-5">
            view all courses
        </button>
    </div>
</template>

<style scoped>
.card {
    border-style: none;
    padding-bottom: 50px;
}

.card img {
    width: 100%;
    margin: auto;
}

.col-2 img {
    width: 70%;
    border-radius: 50%;
}

.card_title {
    width: 70%;
}
</style>