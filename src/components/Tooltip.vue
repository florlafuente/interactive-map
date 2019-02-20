<template>
  <div class="tooltip-container">
    {{ province }}
  </div>
</template>

<script>
  export default {
    name: 'Tooltip',
    props: {
      province: {
        type: String
      }
    }
  }
</script>

<style scoped>
  .tooltip-container {
    position: absolute;
    top: 0;
  }
</style>