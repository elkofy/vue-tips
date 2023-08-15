<template>
    <div class="weird-table">
        <template v-for="data in datas" :key="data.id">
            <slot name="item" v-bind="{ ...data }" />
        </template>
    </div>
</template>

<script setup lang="ts">
import { PropType } from 'vue';

defineProps({
    datas: {
        type: Array as PropType<any[]>,
        required: true
    }
})

</script>

<style scoped>


</style>
