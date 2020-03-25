<template>
  <div class="textbox">
    <label :for="{id}">{{ placeholder }} </label>
    <input :id="{id}" v-model="inputData" type="text" @keyup="$emit('update:inputData', inputData);">
  </div>
</template>

<style lang="scss" src="./index.scss">
</style>

<script>
export default {
  props: {
    id: { type: String, default: '' },
    placeholder: { type: String, default: '' },
    inputData: { type: String, default: '' }
  }
}
</script>
