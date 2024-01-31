<script setup>
import category from '@/assets/category.json'

const categories = category
</script>

<template>
	<li v-for="obj in categories">
		{{obj.name}} - {{obj.image_url}} - {{obj.code}}
	</li>
</template>
