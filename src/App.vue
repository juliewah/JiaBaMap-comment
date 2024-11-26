<template>
  <div>
    <h3>和牛涮 日式鍋物放題 台北羅斯福店的用戶評論</h3>
    <CommentInput @submitComment="addComment" />
    <PreviousReview :comments="comments" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
// 留言框
import CommentInput from './components/CommentInput.vue'
// 先前的評論
import PreviousReview from './components/PreviousReview.vue'

const comments = ref([])

const addComment = (newComment) => {
  comments.value.unshift(newComment)
}
</script>

