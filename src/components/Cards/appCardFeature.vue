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
            <div class="card m-2">
                <img :src="defaultPath + card.srcImg">
                <div class="price">
                    <h3>{{ card.price }}</h3>
                </div>
                <div class="d-flex align-items-center">
                    <div class="col-2 ps-4 pt-3">
                        <img :src="defaultPath + card.userUri">
                    </div>
                    <div class="col-10 pt-3">
                        <span>{{ card.user }}</span>
                    </div>
                </div>
                <h3 class="card_title pt-2 ps-4">{{ card.title }}</h3>
                <div class="data_zone">
                    <div class="col-4 ps-2">
                        <span><i class="ps-3 pe-2 fa-regular fa-file"></i>{{ card.lessons }}</span>
                    </div>
                    <div class="col-4">
                        <span><i class="pe-2 fa-regular fa-user"></i>{{ card.students }}</span>
                    </div>
                </div>
            </div>
        </div>
        <button class="main_btn mx-auto w-25 mt-5">
            view all courses
        </button>
    </div>
</template>

<style scoped>
span {
    color: grey;
    font-size: 15px;
}

h3 {
    font-weight: 700;
}

.card {
    border-style: none;
    padding-bottom: 50px;
    background-color: #f5f5f5;
    height: 489px;
}

.price {
    width: 100px;
    text-align: center;
    background-color: #20ad96;
    color: white;
    padding-top: 7px;
    border-radius: 8px;
    position: absolute;
    top: 0;
    right: 0;
}

.card img {
    width: 100%;
    height: 100%;
    margin: auto;
    border-radius: 8px;
    position: relative;
    filter: blur(1px);
}

.card:hover img {
    filter: blur(0px);
}

.col-2 img {
    width: 70%;
    border-radius: 50%;
}

.card_title {
    width: 70%;
}

.data_zone {
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 20px;
}

.card:hover {
    cursor: pointer;
    box-shadow: 1px 1px 20px 1px;
    transition: 0.4s;
}
</style>