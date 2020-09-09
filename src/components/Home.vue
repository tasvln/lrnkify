<template>
  <div class="hello">
    <div class="top">
    <p class="center header"><b>Lrnk</b>ify</p>
    <p class="center sub">Get links shortened fast & easy</p>
    </div>
    <div class="form">
      <form action="">
        <input class="input" type="text" name="link" id="link" placeholder="Input Link" required>
        <input type="submit" class="short" value="Shorten!">
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
.input{
  width: 100%;
  height: 60px;
  border-radius: 20px;
  font-size: 1.25rem;
  color: #fff;
  font-weight: 500;
  border: none;
  background: rgba(255, 255, 255, 0.5);
  text-align: center;
  outline: none;
}
.short{
  margin: auto;
  display: block;
  margin-top: 2rem;
  background: #D8ACFF;
  border-radius: 100px;
  height: 50px;
  border: none;
  outline: none;
  font-weight: bold;
  font-family: 'Poppins', sans-serif !important;
  width: 150px;
  color: #fff;
  font-size: 1.25rem;
  box-shadow: 0px 4px 10px 2px rgba(216, 172, 255, 0.2);
}
::placeholder{
  font-weight: 500;
  font-size: 1.25rem;
  color: #ffffff;
  font-family: 'Poppins', sans-serif !important;
}
</style>
