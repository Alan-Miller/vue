<template>
  <div>
    <h1 @click='changeName'>My supre cool headre, for {{myName}}</h1>
  </div>
</template>

<script>
  export default {
    props: ['myName'],
    methods: {
      changeName() {
        this.$emit('changeName', 'Hectre')
      }
    }
  }
</script>

<style scoped>
</style>