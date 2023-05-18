
<template>
    <div>
        <input placeholder="Search" class="w-full p-2 dark:bg-slate-600">
    </div>
</template>

<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)

</script>


<style scoped>
</style>
