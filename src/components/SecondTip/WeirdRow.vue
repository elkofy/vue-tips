<template>
    <div class="weird-row">
       <template v-for="item in data" :key="item">
            <div class="weird-row__item">
                {{ item }}
            </div>
        </template>
        <button class="weird-row__item">Hi !</button>
    </div>
</template>

<script setup lang="ts">
defineProps({
    data: {
        type: Object,
        required: true
    }
})
</script>

<style scoped>

</style>
