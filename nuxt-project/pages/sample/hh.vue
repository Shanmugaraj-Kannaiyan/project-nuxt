<template>
  <div>
      <h1>{{name}}</h1>
      <h1>{{age}}</h1>
  </div>
</template>

<script>
export default {
  asyncData({query}) {
      return{
          name:query.name,
          age:query.age
      }
  },
}
</script>

<style>

</style>