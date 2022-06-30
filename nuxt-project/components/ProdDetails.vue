<template>
  <div>
      <h1>{{name}}</h1>
      <h2>{{productName}}</h2>
  </div>
</template>

<script>
export default {
    props: ['name', 'productName']
}
</script>

<style scoped>
h1 {
    padding: 5px;
    border: 1px solid black;
}
</style>