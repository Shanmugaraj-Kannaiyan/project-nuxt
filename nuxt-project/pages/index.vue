<template>
<div class="demo">
<Name/>

<header>
  <div class="title"> NUXT JS</div>
  <nav>
    <nuxt-link to="/">Index</nuxt-link>
       <nuxt-link to="/login">About</nuxt-link>
        <nuxt-link to="/home">Home</nuxt-link>
           <nuxt-link to="/sample/page1">Page</nuxt-link>
  </nav>
</header>

</div>
</template>

<script>
import Name from '../components/Name.vue';
export default {
    components: { Name }
}
</script>

<style>
.demo{
  background-color:white;
}
header{
  padding: 20px;
  background-color:aqua;
  display: flex;
  justify-content: space-between;
  align-items:center;
  box-shadow:0px 3px 6px rgba(0,0, 0,0.1);
}
 header.title{
  color: #212121;
  font-size:24px;
  font-weight:800;
  text-transform: uppercase;
}
nav{
  display: flex;
  align-items: center;
  margin: 0 -15px;
}
nav a{
  display: block;
  margin: 0 30px;
  color: #9f25cf;
} 
</style>