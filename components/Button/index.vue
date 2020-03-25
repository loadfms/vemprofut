
<template>
  <nuxt-link class="button" :class="{ blue: color == 'blue', transparent: color == 'transparent' }" :to="{path}">
    {{ text }}
  </nuxt-link>
</template>

<style lang="scss" src="./index.scss">
</style>

<script>
export default {
  props: {
    text: { type: String, default: 'Button' },
    color: { type: String, default: '' },
    path: { type: String, default: '' }
  }
}
</script>
