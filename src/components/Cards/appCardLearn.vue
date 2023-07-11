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
                <button class="small_btn mt-4 w-50 mx-auto">Start Now</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card {
    border-style: none;
}

.card img {
    width: max-content;
    margin: auto;
}
</style>