<script setup lang="ts">
onMounted(() => {
  console.log('mounted test')
})

onUnmounted(() => {
  console.log('unmounted test')
})

// const { data } = await useAsyncData(() => queryContent('test').findOne())
const data = await queryContent('test').findOne()
</script>

<template>
    <NuxtLink to="/">
        index
    </NuxtLink>
    <ContentRenderer v-if="data" :value="data"/>
</template>