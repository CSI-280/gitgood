<template>
  <div id="body">
      <div class="container">
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
          <br>
          <div id="tableButton">
              <button v-on:click="getToken">Print out animals to console</button>
          </div>

          <div class = "content">
            <div class="image-wrapper">
                <img src="../assets/dogs-and-cats.jpg">
            </div>
            <h1>About Us</h1>
            <p> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Vitae purus faucibus ornare suspendisse sed nisi lacus sed. Dolor sed viverra ipsum nunc aliquet bibendum. Ullamcorper dignissim cras tincidunt lobortis feugiat vivamus. Neque aliquam vestibulum morbi blandit cursus risus. Laoreet non curabitur gravida arcu. Ac tortor vitae purus faucibus ornare suspendisse. Interdum velit euismod in pellentesque massa placerat duis ultricies. Dictum at tempor commodo ullamcorper a lacus vestibulum. Nisl condimentum id venenatis a condimentum vitae sapien pellentesque. Turpis cursus in hac habitasse platea. Imperdiet nulla malesuada pellentesque elit eget gravida cum sociis natoque. Sed euismod nisi porta lorem mollis aliquam ut porttitor leo. Fames ac turpis egestas sed tempus urna. Sociis natoque penatibus et magnis. Pretium fusce id velit ut tortor. Molestie at elementum eu facilisis sed. Purus semper eget duis at. Sed vulputate odio ut enim blandit. Nisl suscipit adipiscing bibendum est ultricies integer quis auctor. </p>
          </div>
      </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .content {
    text-align: center;
  }
  img {
    width: auto;
    height: 20vh;
    border-radius: 2em 2em 2em 2em;
    float: left;
  }
  
</style>

<script>
import { Client } from "@petfinder/petfinder-js";
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Homepage'
    }
  },
    methods: {
        getToken: function () {
            const client = new Client({ apiKey: "HB4E0LPBodtgXJlBVOYvZSDaxgGSCA7Li7Eq6tqb6uVDRfzAp4", secret: "ACCq1YmJ2XzZxT6WrvbSU9voepnbCllw0NmSF363" });

            client.animal.search()
                .then(function (response) {
                    // Do something with resp.data.animals
                    console.log(response.data.animals)
                });
        }
    }
}
</script>