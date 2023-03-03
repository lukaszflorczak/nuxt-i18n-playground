<template>
  <div>
    <button
      v-for="locale in $i18n.locales"
      :key="locale.code"
      @click="$i18n.setLocale(locale.code)"
    >
      {{ locale.name }}
    </button>
  </div>

  <nuxt-page />

  <p>
    Test:
    <nuxt-link to="/disabled-localized-route">
      Page with disabled localized route
    </nuxt-link>
  </p>
</template>

<style lang="css" scoped>
button {
  margin-right: 16px;
}
</style>
