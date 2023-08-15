<template>
  <h1>Vue Tips by @nassbin</h1>

  <div>
    <h2>Tips 1: Keep it simple</h2>
    <GPComponent />
  </div>
  <div>
    <h2>Tips 2: Unleash the power of templating</h2>
    <WeirdList />
  </div>
  <div>
    <h2>Tips 3: Array to display</h2>
    <CommentList />
  </div>

</template>

<script setup lang="ts">
import GPComponent from './components/FirstTip/GPComponent.vue';
import WeirdList from './components/SecondTip/WeirdList.vue';
import CommentList from './components/ThirdTip/CommentList.vue';
</script>

<style scoped></style>
