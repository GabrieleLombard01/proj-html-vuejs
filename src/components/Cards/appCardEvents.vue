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

    </div>
</template >
