<template>
    <div class="comment-card">
        <div v-for="info in comment" >
        <p v-if="!info.toString().endsWith('.com')">{{ info }}</p>
        </div>
    </div>
</template>

<script setup lang="ts">

import { PropType } from 'vue';

defineProps({
    comment: {
        type: Object as PropType<any>,
        required: true
    }
})

</script>

<style scoped>
.comment-card {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding: 1rem;
    border: 1px solid #ccc;
    border-radius: 0.5rem;
}
.comment-card__header {
    display: flex;
    gap: 1rem;
}


.comment-mail {
    font-size: 0.8rem;
    color: #ccc;
}


.comment-card__header__name {
    font-weight: bold;
}

.comment-card__body {
    font-size: 0.9rem;
}
</style>