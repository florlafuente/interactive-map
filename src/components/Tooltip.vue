<template>
  <div class="tooltip-container">
    {{ province }}
    <ul>
      <li v-for="(indicator, key) in info.indicators" :key="key">
        {{indicator.name}}: {{indicator.value}}
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'Tooltip',
    props: {
      province: {
        type: String
      },
      info: {
        type: Object
      }
    },
    mounted () {
      console.log(this.info)
    }
  }
</script>

<style scoped>
  .tooltip-container {
    background: #ffffff;
    border: 1px solid #f38eb0;
    height: 150px;
    left: 400px;
    top: 200px;
    padding: 20px;
    position: absolute;
    width: 300px;
  }
</style>