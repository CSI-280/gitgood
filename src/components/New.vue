<template>
    <body>
        <h1> This is a new page </h1>
        <router-link to="/Home">
            <button>Navigate back to home</button>
        </router-link>
    </body>
</template>

<script>
    export default {
        name: 'New',
        data () {
            return {
                msg: 'This is a new page'
            }
        }
    }
</script>

<style scoped>
    body {
      font-family: 'Roboto', sans-serif;
      color:#282828;
      background: #FFFFFF;
      padding:0;
      margin:0;
      text-align:center;
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