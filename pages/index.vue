<script setup lang="ts">
onMounted(() => {
  console.log('mounted index')
})

onUnmounted(() => {
  console.log('unmounted index')
})

// const { data } = await useAsyncData(() => queryContent('home').findOne())
const data = await queryContent('home').findOne()
</script>

<template>
    <NuxtLink to="/test">
        test
    </NuxtLink>
    <ContentRenderer v-if="data" :value="data"/>
</template>