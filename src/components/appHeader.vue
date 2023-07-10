<script>
export default {
    data() {
        return {
            HeaderNav: [
                {
                    "home": "Home 🡣",
                    "pages": "Pages 🡣",
                    "courses": "Courses 🡣",
                    "features": "Features 🡣",
                    "blog": "Blog 🡣",
                    "shop": "Shop 🡣",
                }
            ],
        };
    },
};
</script>

<template>
    <div class="margin_contents d-flex justify-content-between align-items-center ps-3 pe-3">
        <div class="col-4">
            <img class="w-50" src="../assets/img/dark-logo.png" alt="logo">
        </div>
        <div class="col-8">
            <ul>
                <li v-for="(item, index) in HeaderNav[0]" :key="index">
                    <a href="#">{{ item }}</a>
                </li>
            </ul>
        </div>
    </div>
</template>