<template>
  <div></div>
</template>

<script>
export default {
  async created() {
    await this.$auth.logout()
  }
}
</script>
  
  <style scoped>
  
  </style>