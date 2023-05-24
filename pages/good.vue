<template>
  <div>GOOD</div>
  <div>Story ID: {{ story.id }}</div>
  <div>Story Name: {{ story.name }}</div>
</template>

<script setup>
const params = { version: process.env.NODE_ENV !== 'production' ? 'draft' : 'published', language: 'en' }
const storyblokApi = useStoryblokApi()
const { data } = await useAsyncData('home', async () => await storyblokApi.get('cdn/stories/home', params))
const story = toRef(data.value.data.story)

const { query } = useRoute()
onMounted(() => {
  if (!!query._storyblok) {
    useStoryblokBridge(story.value.id, (evStory) => (story.value = evStory))
  }
})
</script>
