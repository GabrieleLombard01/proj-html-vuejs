<script>
import { data } from "../../data/index";

export default {
    data() {
        return {
            cards: [
                ...data.firstCard,
                ...data.secondCard,
                ...data.thirdCard,
                ...data.fourthCard,
            ],
            defaultPath: "/src/assets/img/",
        };
    },
};
</script>

<template>
    <div class="row">
        <div class="col-3 pt-5" v-for="(card, index) in cards" :key="index">
            <div class="card">
                <img :src="defaultPath + card.srcImg">
                <h6 class="pt-4">{{ card.title }}</h6>
                <span class="pt-3">{{ card.descr }}</span>
                <button class="small_btn mt-3 mb-3 w-50 mx-auto">Start Now<i
                        class="ps-2 fa-solid fa-arrow-right fa-lg"></i></button>
            </div>
        </div>
    </div>
</template>

<style scoped>
h6 {
    font-weight: 700;
    font-size: 18px;
}

span {
    color: grey;
}

.card {
    border-style: none;
}

.card img {
    width: max-content;
    margin: auto;
}

.small_btn {
    color: rgb(94, 94, 94);
    padding: 5px 10px 5px 10px;
    border-style: none;
    background-color: white;
    border-radius: 5px;
    font-weight: 700;
}

.small_btn:hover {
    background-color: rgb(218, 218, 218);
}
</style>