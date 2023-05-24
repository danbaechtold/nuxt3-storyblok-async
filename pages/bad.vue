<template>
  <div>BAD</div>
  <div>Story ID: {{ story.id }}</div>
  <div>Story Name: {{ story.name }}</div>
</template>

<script setup>
const params = { version: process.env.NODE_ENV !== 'production' ? 'draft' : 'published', language: 'en' }
const story = await useAsyncStoryblok('home', params)
</script>
