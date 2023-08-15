<template>
    <div class="comment-list">
        <template v-for="comment in comments" :key="comment.id">
            <Comment :comment="comment" />
        </template>
    </div>
</template>

<script setup lang="ts">
import Comment from './CommentCard.vue';
import { ref } from 'vue';

const comments = ref([]);
fetch('https://jsonplaceholder.typicode.com/comments')
    .then(response => response.json())
    .then(json => {
        console.log(json);
        comments.value = json;
    })
</script>