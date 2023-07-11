<template>
  <h1>Dashboard</h1>

  <p>
    <nuxt-link :to="localePath('/')">Back to home</nuxt-link>
  </p>
</template>

<script lang="ts" setup>
  defineI18nRoute(false)
</script>
