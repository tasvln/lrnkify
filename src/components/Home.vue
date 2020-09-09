<template>
  <div class="hello">
    <div class="top">
    <p class="center header"><b>Lrnk</b>ify</p>
    <p class="center sub">Get links shortened fast & easy</p>
    </div>
    <div class="form">
      <form action="">
        <input type="text" name="link" id="link" placeholder="Input Link">
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.center{
  text-align: center;
  color: #fff;
}
.top{
  margin-top: 4rem;
}
.header{
  font-size: 3rem;
}
.sub{
  margin-top: 10px;
  font-size: 1.5rem;
  font-weight: 300;
}
form{
  max-width: 500px;
  margin: auto;
  display: block;
  margin-top: 4rem;
}
@media screen and (max-width: 900px) {
  .form{
    margin: 0 15px;
  }
}
input{
  width: 100%;
  height: 60px;
  border-radius: 20px;
  border: none;
  text-align: center;
  outline: none;
}
</style>
