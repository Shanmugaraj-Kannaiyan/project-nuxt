<template>
  <div>
      <input type="text"  v-model="data">
      <ProdDetails :name='data' :productName='data1'/>
  </div>
</template>

<script>
export default {
    data(){
        return {
            data: '',
            data1: 'Better Product'
        }
    }
}
</script>

<style>

</style>