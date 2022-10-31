<template>
    <input 
      type="text" 
      placeholder="Enter color" 
      v-model="$store.state.colorCode"
    />
</template>

<script>
export default {
  computed: {
    colorCode: {
      get() {
        return this.$store.state.colorCode
      },
      set(newValue) {
        this.$store.dispatch('setColorCode', newValue)
      }
    }
  } 
}
</script>

<style>

</style>