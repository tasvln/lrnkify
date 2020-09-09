<template>
  <div class="hello">
    <div class="top">
    <p class="center header"><b>Lrnk</b>ify</p>
    <p class="center sub">Get links shortened fast & easy</p>
    </div>
    <div class="form">
      <form action="">
        <input class="input" type="text" name="link" id="link" placeholder="Input Link" required>
        <button class="short">Shorten!</button>
      </form>
    </div>
    <div class="box">
      <div class="link">Link</div>
      <a class="lrnk" href="">https://lrnk.ify/3443</a>
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
  background-color: #734B97;
  border-radius: 100px;
  height: 50px;
  border: 4px solid #D8ACFF;
  outline: none;
  font-weight: bold;
  font-family: 'Poppins', sans-serif !important;
  width: 150px;
  color: #fff;
  font-size: 1.25rem;
}
::placeholder{
  font-weight: 500;
  font-size: 1.25rem;
  color: #ffffff;
  font-family: 'Poppins', sans-serif !important;
}
.box{
  max-width: 400px;
  margin: auto;
  display: block;
  margin-top: 4rem;
  background-color: #D8ACFF;
  border-radius: 1000px;
  padding: 20px 40px;
  text-align: center;
}
.link{
  padding: 4px 5px;
  background-color: #fff;
  max-width: 80px;
  margin: auto;
  display: block;
  font-weight: bold;
  border-radius: 100px;
  color: #734B97;
  font-family: 'Poppins', sans-serif !important;
  margin-bottom: 1.5rem;
}
.lrnk{
  font-weight: 600;
  color: #734B97;
}
@media (min-width: 320px) and (max-width: 500px){
  .form{
    margin: 0 15px;
  }
  .center{
    margin: 0 20px;
  }
  .box{
    margin: 0 20px;
    margin-top: 3rem;
    margin-bottom: 4rem;
  }
}
</style>
