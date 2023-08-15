<template>
    <h5>Parent Component 👨</h5>
    <button @click="throwBall">pass</button>

    <div v-if="ball && !passedBall">
        <h6>🙌 {{ ball }}</h6>
    </div>

    <CComponent :ball="passedBall" @pass="emitEvent" />
</template>

<script setup lang="ts">
import { ref } from 'vue';
import CComponent from './CComponent.vue';
const passedBall = ref('');
const emit = defineEmits(['pass'])
defineProps({
    ball: {
        type: String,
        default: '🏀'
    }
})
const throwBall = () => {
    passedBall.value = '🏀';
}
const emitEvent = (value: string) => {
    console.log(value);
    emit('pass', value)
}



</script>