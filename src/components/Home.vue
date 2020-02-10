<template>
  <div id="body">
    
    <div class="container">  
      <h2>This is the site for the gitgood team</h2>
      <router-link to="/New">
        <button>Navigate to a new page</button>
      </router-link>
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
