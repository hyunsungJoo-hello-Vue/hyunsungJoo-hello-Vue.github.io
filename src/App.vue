<script setup>
import { ref } from 'vue'
import sportsData from '@/assets/sports.json'

const showChosunData = ref(true)
const all = sportsData

const filterChosunData = () => {
  return sportsData.articles.filter(article => article.source?.name === 'Chosun.com')
}

const chosunArticles = filterChosunData()
</script>

<template>
  <div>
    <button @click="showChosunData = !showChosunData">조선일보 기사만 보기</button>
    <ul v-if="showChosunData">
        <li v-for="article in all.articles"> <!-- 수정된 부분 -->
        {{ article.author }} - {{ article.title }} - {{ article.url }}
        </li>
    </ul>

    <ul v-else>
      <li v-for="article in chosunArticles">
        {{ article.author }} - {{ article.title }} - {{ article.url }}
      </li>
    </ul>
  </div>
</template>
