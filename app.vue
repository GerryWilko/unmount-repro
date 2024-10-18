<script setup lang="ts">
onMounted(() => {
  console.log('mounted app')
})

onUnmounted(() => {
  console.log('unmounted app')
})
</script>

<template>
  <NuxtPage/>
</template>
