<script setup>
import category from '@/assets/sports.json'

const categories = sports
</script>

<template>
        <button @click="awesome = !awesome">toggle</button>

        <h1 v-if="awesome">Vue is awesome!</h1>
        <h1 v-else>Oh no 😊</h1>
</template>
