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
        </div>
        <div id="pfData">
        </div>
    </div>
</template>

<script src="https://code.jquery.com/jquery-3.4.1.js">
  import { Client } from "@petfinder/petfinder-js";
  import { Animal } from '@petfinder/petfinder-js/dist/api/animal';

  export default {
  name: 'Cats',
  data () {
      return {
      msg: 'Catspage'
      }
  },
      methods: {
          getToken: function () {
              const client = new Client({ apiKey: "HB4E0LPBodtgXJlBVOYvZSDaxgGSCA7Li7Eq6tqb6uVDRfzAp4", secret: "ACCq1YmJ2XzZxT6WrvbSU9voepnbCllw0NmSF363" });
              var output = document.getElementById("pfData");
              format = JSON;

              $(document).ready(function () {
                $.getJSON(Client, function(data) {
                  var cat_data = '';
                  $.each(data, function(key, value) {
                    cat_data += '<tr>';
                    cat_data += '<td>' + value.name + '</td>';
                    cat_data += '<td>' + value.animal + '</td>';
                    cat_data += '<td>' + value.breed + '</td>';
                    cat_data += '<td>' + value.shelterid + '</td>';
                    cat_data += '<td>' + value.primaryphoto + '</td>';
                    cat_data += '</tr>';
                  })
                })
              });
              console.log("hi")
              console.log(client$pet.getRandom(output = 'basic'))
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