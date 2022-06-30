<template>
  <div>
    <h1>NUXT</h1>
    <p>NAME:<input type="text" v-model="name"></p>
    <!-- <p>AGE:<input type="number" v-model="age"></p> -->
    <!-- <button @click="send()">send</button> -->
    {{name}}
    <div>
      <p v-if="name == 'james'">I am a Handsome boy</p>
      <p v-else>I am a Beautiful girl</p>
    </div>
  </div>

</template>

<script>

export default {
  data(){
    return {
      name: ''
    }
  },
  methods:{
    send(){
      if(!this.name&&this.age){
        return
      }
   //this.$nuxt.$router.push({path:'/sample/hh?name='+this.name+'&age='+this.age})
      // this.$nuxt.$router.push({path:'/sample/' + this.name})
    }
  }
}

</script>

<style>

</style>