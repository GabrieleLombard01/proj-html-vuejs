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
                    <span>{{ card.position }}</span>
                    <h3>{{ card.title }}</h3>
                </div>
                <div class="col-3 text-center">
                    <h1>{{ card.day }}</h1>
                    <span>{{ card.month }}</span>
                    <div class="main_btn">Get ticket</div>
                </div>
            </div>
        </div>
    </div>
    <h3 class="text-center pt-5"><a href="#">Excited about our event? View all events</a></h3>
</template >

<style scoped>
.long_card {
    margin: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #f8f8f8;
    border-radius: 10px;
    padding: 20px;
}
</style>
