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
    background: #ffffff;
    border: 1px solid #f38eb0;
    height: 150px;
    left: 400px;
    padding: 20px;
    position: absolute;
    width: 300px;
  }
</style>