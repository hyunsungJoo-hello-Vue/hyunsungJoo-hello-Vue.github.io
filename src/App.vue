<script setup>
import { ref } from 'vue'
const message = ref({name: "JOO", age:28})
</script>

<template>
	<h1>{{ message }}</h1>
</template>
