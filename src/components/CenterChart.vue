
<template>
    <div>
        <Chart :options="{ theme: 'dark', }"
        />
    </div>
</template>

<script>
import { Chart } from 'vue-tradingview-widgets';

import {defineComponent, ref} from 'vue'
//
// defineProps({
//     msg: String,
// })

const count = ref(0)


export default defineComponent({
    name: 'App',
    components: {
        Chart,
    },
});


</script>


<style scoped>
</style>
