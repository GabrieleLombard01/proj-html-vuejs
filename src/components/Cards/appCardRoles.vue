<script>
import { data } from "../../data/index";
export default {
    data() {
        return {
            cards: [
                ...data.firstCardRoles,
                ...data.secondCardRoles,
                ...data.thirdCardRoles,
            ],
            defaultPath: "/src/assets/img/",
        };
    },
};
</script>

<template>
    <div class="margin_content">
        <div class="row">
            <div class="col-4" v-for="(card, index) in cards" :key="index">
                <div class="role_card text-center">
                    <img :src="defaultPath + card.srcImg" :alt="card.name">
                    <p>{{ card.decr }}</p>
                    <h6>{{ card.name }}</h6>
                    <span>{{ card.role }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.role_card img {
    width: 40%;
    border-radius: 50%;
}
</style>