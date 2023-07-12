<script>
import { data } from "../data/index";
export default {
    data() {
        return {
            cards: [
                ...data.firstCardGrid,
                ...data.secondCardGrid,
                ...data.thirdCardGrid,
                ...data.fourthCardGrid,
                ...data.fifthCardGrid,
                ...data.sixthCardGrid,
                ...data.seventhCardGrid,
                ...data.eigthCardGrid,
                ...data.ninthCardGrid,
                ...data.tenthCardGrid,
                ...data.eleventhCardGrid,
                ...data.twelfthCardGrid,
            ],
            defaultPath: "/src/assets/img/",
        };
    },
};
</script>

<template>
    <div class="grid_container p-4">
        <div class="row">
            <div class="col-6 pb-4" v-for="(card, index) in cards" :key="index">
                <img :src="defaultPath + card.srcImg" :alt="card.name">
            </div>
        </div>
    </div>
</template>

<style scoped>
.grid_container {
    width: 100%;
    height: 78vh;
    overflow-y: scroll;

}

.col-6 img {
    border: solid rgb(224, 224, 224) 1px;
    cursor: pointer;
}

.col-6 img:hover {
    box-shadow: 1px 1px 10px 1px rgb(189, 189, 189);
}
</style>