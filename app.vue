<template>
  <div class="row">
    <code>switchLocalePath()</code>

    <nuxt-link
      v-for="locale in $i18n.locales"
      :key="locale.code"
      :to="switchLocalePath(locale.code)"
    >
      {{ locale.name }}
    </nuxt-link>
  </div>

  <div class="row">
    <code>setLocale()</code>

    <button
      v-for="locale in $i18n.locales"
      :key="locale.code"
      @click="$i18n.setLocale(locale.code)"
    >
      {{ locale.name }}
    </button>
  </div>

  <nuxt-page />
</template>

<script lang="ts" setup>
  const switchLocalePath = useSwitchLocalePath()
</script>

<style lang="css" scoped>
  .row {
    align-items: center;
    display: flex;
    gap: 20px;
    margin-bottom: 20px;
  }
</style>
