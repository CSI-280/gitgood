<template>
  <div id="body">
    <div class="top-title">
      <h1>git-a-pet</h1>
    </div>
    <div class="container">  
        <h2>This is the site for the gitgood team</h2>
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

  .top-title { 
      height: 80px;
      text-align: center;
      color:#FFFFFF;
      font-size: 30px;   
  }

    .container {
      margin: auto;
      width: 60%;
      height: 70.5vh;
      float: center;
      border-radius: 2em 2em 0em 0em;
      background: white;
      padding: 1%;
  }




</style>
