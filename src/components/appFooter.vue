<script>
import { data } from '../data/index.js';

export default {
    computed: {
        firstCol() {
            return data.firstCol[0];
        },
        secondCol() {
            return data.secondCol[0];
        },
        thirdCol() {
            return data.thirdCol[0];
        },
        fourthCol() {
            return data.fourthCol[0];
        }
    }
};
</script>

<template>
    <div class="footer">
        <div class="margin_contents">
            <div class="row justify-content-between">
                <div class="col-4">
                    <h4 class="pb-2">{{ firstCol.title }}</h4>
                    <h6>{{ firstCol.firstRow }}</h6>
                    <h6>{{ firstCol.secondRow }}</h6>
                    <h6>{{ firstCol.thirdRow }}</h6>
                </div>
                <div class="col-2">
                    <h4 class="pb-2">{{ secondCol.title }}</h4>
                    <h6>{{ secondCol.firstRow }}</h6>
                    <h6>{{ secondCol.secondRow }}</h6>
                    <h6>{{ secondCol.thirdRow }}</h6>
                </div>
                <div class="col-2">
                    <h4 class="pb-3">{{ thirdCol.title }}</h4>
                    <h6 class="pt-4">{{ thirdCol.firstRow }}</h6>
                    <h6>{{ thirdCol.secondRow }}</h6>
                    <h6>{{ thirdCol.thirdRow }}</h6>
                </div>
                <div class="col-2">
                    <h4 class="pb-2">{{ fourthCol.title }}</h4>
                    <h6>{{ fourthCol.firstRow }}</h6>
                    <h6>{{ fourthCol.secondRow }}</h6>
                    <h6>{{ fourthCol.thirdRow }}</h6>
                    <h6>{{ fourthCol.fourthRow }}</h6>
                </div>
            </div>
        </div>
        <!--details-->
        <div class="margin_contents fs-2 mb-5">
            <i class="fa-brands fa-square-facebook pe-2"></i>
            <i class="fa-brands fa-square-twitter pe-2"></i>
            <i class="fa-brands fa-instagram pe-2"></i>
            <i class="fa-brands fa-linkedin pe-2"></i>
        </div>
        <!---->
        <div class="margin_contents text-center">
            <span>© 2020 Maxcoach. All Rights Reserved</span>
        </div>
    </div>
</template>

<style scoped>
h4 {
    font-weight: 700;
    font-size: 20px;
}

h6 {
    padding-bottom: 5px;
    color: grey;
    font-size: 14px;
    font-weight: 600;
}

span {
    color: grey;
    font-weight: 600;
}

h6:hover {
    color: #20ad96;
    cursor: pointer;
    text-decoration: underline;
}

.footer {
    margin-top: 40px;
    padding: 20px;
    min-height: 300px;
    width: 100%;
    background-color: white;
}

.margin_contents i {
    color: grey;
}

.margin_contents i:hover {
    color: #20ad96;
    cursor: pointer;
}
</style>