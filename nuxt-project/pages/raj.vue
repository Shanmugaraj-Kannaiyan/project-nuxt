<template>
  <div>
      <input type="text" v-model="name">
      <p>{{name}}</p>
        <p v-if="name =='raj'">Welcome to Nuxt js</p>
        <p v-else>Welcome to vue js</p>

  </div>
</template>

<script>
export default {
  data(){
      return{
          name:''
      }
  }
}
</script>

<style>

</style>