<template>
    <h4>Grand-Parent Component 👴</h4>
    <button @click="throwBall">pass</button>
    <div v-if="isThrowed">
        <h5>🙌 🏀</h5>
    </div>
    <PComponent :key="rerender" :ball="ball" @pass="receiveBall" />
</template>

<script setup lang="ts">
import { ref } from 'vue';
import PComponent from './PComponent.vue';
let ball = ref('');
let rerender = ref(0);
let isThrowed = ref(true);
const throwBall = () => {

    ball.value = '🏀';
    isThrowed.value = false;
    rerender.value++;

}


const receiveBall = () => {
    ball.value = '';
    isThrowed.value = true;
    rerender.value++;

}



</script>