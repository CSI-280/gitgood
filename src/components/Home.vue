<template>
  <body>
        <div class="nav-bar">
            <div class="top-title">
                <h1>git-a-pet</h1>
            </div>
        </div>
        <h2>This is the site for the gitgood team</h2>
        
        <router-link to="/New">
          <button>Navigate to new page</button>
        </router-link>
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
      font-family: 'Roboto', sans-serif;
      color:#282828;
      background: #FFFFFF;
      padding:0;
      margin:0;
      text-align:center;
  }

  .nav-bar {
      background: linear-gradient(-90deg, #febc55, #ff6969, #9500ff);
      height: 80px;
  }

  .top-title {
      font-family: 'Roboto', sans-serif;
      text-align: center;
      color:#FFFFFF;
      font-size: 30px;   
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
</style>
