<template>

    <div id="body">
        <div class="container">  
          <h1>Find the Cat For You!</h1>
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
          <h3>
          <p>This box will expand as stuff is added.</p>
          </h3>
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