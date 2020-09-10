<template>
  <div class="hello">
    <div class="top">
    <p class="center header"><b>Lrnk</b>ify</p>
    <p class="center sub">Get links shortened fast & easy</p>
    </div>
    <div class="form">
      <form method="post" @submit.prevent="trimUrl">
        <input class="input" type="url" name="url" id="url" placeholder="https://link.domain" v-model="url" required>
        <button class="short">Shorten!</button>
      </form>
    </div>
    <div class="box" v-if="isReady">
      <div class="link">Link</div>
      <a :href="linkUrl"  target="_blank" class="lrnk">{{ linkUrl }}</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',

  data() {
        return {
          url: '',
          isReady: false,
          linkUrl: '',
        }
    },
    methods: {
      trimUrl() {
          if (this.url == "") {
            this.er = true;
          }
            this.isReady = false;
            this.$http.post('https://rel.ink/api/links/', {"url": this.url})
            .then(res=> {
                this.isReady = true;
                this.linkUrl = `https://rel.ink/${res.body.hashid}`;
                this.mainUrl = `${res.data.url}`;
                localStorage.setItem("links", JSON.stringify(this.links));
                let data = {
                  parsedUrl : `https://rel.ink/${res.body.hashid}`,
                  urlLink: `${res.data.url}`
                };
                this.links.unshift(data);
            })
        },
        getLinks() {       
            if (localStorage.getItem('links')) this.links = JSON.parse(localStorage.getItem('links'));
        }
    },
    mounted() {
        this.getLinks();
}
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
  border: 2px solid #D8ACFF;
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
.short:focus, .short:hover{
  border: 4px solid #D8ACFF;
  cursor: pointer;
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
