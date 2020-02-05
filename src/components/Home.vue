<template>
  <body>
    <div class="top-title">
      <h1>git-a-pet</h1>
    </div>
    <div class="nav-bar">   
        <h2>hi</h2>   
        <!--Nav bar goes here -->
    </div>
    <div class="container">  
        <h2>This is the site for the gitgood team</h2>

        <router-link to="/New">
          <button>Navigate to new page</button>
        </router-link>

    </div>
  </body>
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
  body {
      height: 100%;
      font-family: 'Roboto', sans-serif;
      color:#282828;
      background: #FFFFFF;
      padding:0;
      margin:0;
      text-align:center;
      background: linear-gradient(-90deg, #febc55, #ff6969, #9500ff);
  }

  .top-title { 
      height: 80px;
      font-family: 'Roboto', sans-serif;
      text-align: center;
      color:#FFFFFF;
      font-size: 30px;   
  }

  .nav-bar {
    height: 5%;
    color: white;
  }

  button {
      margin-top: 20px;
      border: none;
      background-color: #ff6969;
      color: white;
      height: 60px;
      width: 180px;
      font-size: 16px;
      border-radius: 15px;
  }

  .container {
      margin: auto;
      width: 60%;
      height: 80%;
      float: center;
      border-radius: 2em 2em 0em 0em;
      background: white;
      padding: 1%;
  }

  .cr-info {
    color: white;
  }
</style>
