<script setup>
import HomePage from './pages/HomePage.vue'
import BaseLayout from './components/BaseLayout.vue'
import BaseButton from './components/BaseButton.vue'

</script>

<template>
  <div>
    <BaseLayout>
      <HomePage />
      <BaseButton dangerValue="danger"/>
    </BaseLayout>
  </div>
</template>

<style scoped>
</style>
