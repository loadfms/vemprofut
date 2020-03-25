<template>
  <div class="home_container">
    <div>
      <h1 class="title">
        VEM PRO
      </h1>
      <h2 class="subtitle">
        FUT
      </h2>
      <div class="links">
        <Button text="Login com email" />
        <Button text="Login com facebook" color="blue" />
        <Button text="cadastre-se" color="transparent" path="/signup" />
      </div>
    </div>
  </div>
</template>

<script>
import Button from '~/components/Button/'

export default {
  components: {
    Button
  }
}
</script>

<style lang="scss" src="./index.scss">
</style>
