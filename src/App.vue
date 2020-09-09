<template>
  <div id="app">
    <Home/>
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
body{
  background-color: #734B97 !important;
  background: url(https://res.cloudinary.com/dudhmrdin/image/upload/v1599663133/MacBook_Pro_-_3_sqdxae.svg);
  font-family: 'Poppins', sans-serif !important;
  scroll-behavior: smooth;
}
a,p,h1,h2,h3,h4,h5,h6{
  font-family: 'Poppins', sans-serif;
}
a{
  text-decoration: none;
}
</style>
