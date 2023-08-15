<template>
    <h6>Child Component  </h6>
    <div v-if="ball && !passedBall">
        <h6>🙌 {{ball}}</h6>
    </div>
    <button @click="throwBall">pass</button>

</template>

<script setup lang="ts">
import { ref } from 'vue';

const  emit = defineEmits(['pass'])
 const props = defineProps({
    ball:{
        type:String,
        default:'🏀'
    }
})

const passedBall = ref(props.ball ?? '');
const throwBall = () => {
    passedBall.value = '🏀';
    emit('pass',passedBall.value)

}

</script>