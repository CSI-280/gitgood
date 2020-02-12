<template>
  <div id="body">
    
    <div class="container">  
      <h1>Welcome to the GitGood Adoption Site!</h1>
      <router-link to="/Home">
        <button>Home</button>
      </router-link>
      <router-link to="/Dogs">
        <button>Dogs</button>
      </router-link>
      <router-link to="/Cats">
        <button>Cats</button>
      </router-link>
      <router-link to="/Other">
        <button>Other</button>
      </router-link>
      <p>text here...</p>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <p>text in between...</p>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <p>text in between...</p>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <p>text in between...</p>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <br>
      <p>end of text.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Homepage'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #body {
      height: 80%;
      color:#282828;
      background: #FFFFFF;
      padding:0;
      margin:0;
      text-align:center;
      background: linear-gradient(-90deg, #febc55, #ff6969, #9500ff);
  }
  
</style>
