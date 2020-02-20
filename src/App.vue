<template>
  <div id="app">
    <link href="https://fonts.googleapis.com/css?family=Roboto:100&display=swap" rel="stylesheet">
    <router-link to="/Home">
      <button>Home</button>
    </router-link>
    <router-link to="/Dogs">
      <button>Dogs</button>
    </router-link>
    <router-link to="/Cats">
      <button>Cats</button>
    </router-link>
    <router-link to="/About">
      <button>About</button>
    </router-link>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  #app {
    padding:0;
    margin:0;
  }
</style>
