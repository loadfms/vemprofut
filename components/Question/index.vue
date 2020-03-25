
<template>
  <div class="question">
    <p class="text">{{text}}</p>
    <p class="helptext">{{helptext}}</p>
  </div>
</template>

<style lang="scss" src="./index.scss">
</style>

<script>
export default {
  props: {
    text: String,
    helptext: String
  }
}
</script>
