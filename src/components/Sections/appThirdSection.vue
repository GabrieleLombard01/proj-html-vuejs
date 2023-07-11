<script>
import appTitle from '../appTitle.vue';
import { data } from '../../data/index.js';

export default {
    components: { appTitle },
    computed: {
        titleThirdSection() {
            return data.titleThirdSection[0];
        },
    },
};
</script>