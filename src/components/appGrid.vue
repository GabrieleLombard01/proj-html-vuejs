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
            showOverlays: Array.from({ length: 12 }, () => false),
        };
    },
    methods: {
        showOverlay(index) {
            this.showOverlays = this.showOverlays.map((value, i) => (i === index ? true : value));
        },
        hideOverlay(index) {
            this.showOverlays = this.showOverlays.map((value, i) => (i === index ? false : value));
        },
    },
};
</script>

<template>
    <div class="grid_container mt-3 pt-5 p-4">
        <div class="row">
            <div class="col-6 pb-4" v-for="(card, index) in cards" :key="index">
                <div class="image-container">
                    <img :src="defaultPath + card.srcImg" :alt="card.name" @mouseover="showOverlay(index)"
                        @mouseout="hideOverlay(index)">
                    <div class="overlay text-center" :class="{ 'show': showOverlays[index] }">{{ card.title }}</div>
                </div>
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

.image-container {
    position: relative;
    display: inline-block;
}

.overlay {
    position: absolute;
    background-color: rgba(0, 0, 0, 0.799);
    width: 120px;
    height: 50px;
    top: -20%;
    left: 7.5%;
    opacity: 0;
    transition: opacity 0.3s;
    border-radius: 5px;
    color: white;
    padding-top: 12px;
    font-weight: 700;
}

.overlay.show {
    opacity: 1;
}
</style>