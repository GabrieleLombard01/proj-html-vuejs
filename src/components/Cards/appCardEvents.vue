<script>
import { data } from "../../data/index";

export default {
    data() {
        return {
            cards: [
                ...data.firstCardEvents,
                ...data.secondCardEvents,
                ...data.thirdCardEvents,
                ...data.fourthCardEvents,
                ...data.fifthCardEvents,
                ...data.sixthCardEvents
            ],
        };
    },
};
</script>

<template>
    <div class="row">
        <div class="col-6 pt-5" v-for="(card, index) in cards" :key="index">
            <div class="long_card">
                <div class="col-9">
                    <span class="pos">{{ card.position }}</span>
                    <h3 class="mt-3">{{ card.title }}</h3>
                </div>
                <div class="col-3 text-center">
                    <h1>{{ card.day }}</h1>
                    <span>{{ card.month }}</span>
                    <div class="main_btn mt-2">Get ticket</div>
                </div>
            </div>
        </div>
    </div>
    <div class="text-center p-5">
        <h4 class="text-center pt-5 pe-2 d-inline">Excited about our event?</h4>
        <a class="d-inline" href="#">View all events -></a>
    </div>
</template >View all events

<style scoped>
h1 {
    color: #20ad96;
}

h3 {
    font-weight: 900;
}

h4 {
    font-weight: 600;
    color: grey;
    font-size: 17px;
}

a {
    color: #20ad96;
    font-weight: 800;
}

a:hover {
    text-decoration: underline;
}

.long_card {
    margin: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #f8f8f8;
    border-radius: 10px;
    padding: 5px 20px 10px 20px;
    font-weight: 700;
}

.pos {
    font-weight: 600;
    color: grey;
}
</style>
