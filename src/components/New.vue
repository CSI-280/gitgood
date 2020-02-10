<template>

    <div id="body">
        <div class="container">
            <h1> This is a new page </h1>
            <router-link to="/Home">
                <button>Navigate back to home</button>
            </router-link>
        </div>
    </div>
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