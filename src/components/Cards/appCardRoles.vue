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
        <!--GRID:-->
        <div class="row">
            <div class="col-4" v-for="(card, index) in cards" :key="index">
                <div class="role_card text-center">
                    <img :src="defaultPath + card.srcImg" :alt="card.name">
                    <p class="pt-3">{{ card.decr }}</p>
                    <h6>{{ card.name }}</h6>
                    <span>{{ card.role }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
p {
    font-weight: 700;
    color: #3f3a64;
}

h6 {
    font-weight: 800;
}

span {
    color: grey;
    font-size: 14px;
}



.role_card {
    background-color: white;
    box-shadow: 1px rgb(213, 212, 212);
    border-radius: 10px;
    position: relative;
    min-height: 270px;
    padding: 90px 15px 15px 15px;
    margin-top: 130px;
}

.role_card img {
    width: 40%;
    border-radius: 50%;
    position: absolute;
    top: -25%;
    left: 30%;
}
</style>