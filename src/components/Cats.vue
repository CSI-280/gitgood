<template v-on:load="getCats(), getToken()">

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
          <div id="pfData">
          </div>
          <button v-on:click="getCats(), getToken()">Generate</button>
          <p>Contact Us For Help and More Information About Our Pets!</p>
        </div>
    </div>
</template>

<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
<script src="https://unpkg.com/@petfinder/petfinder-js/dist/petfinder.min.js"></script>
<script src="https://unpkg.com/@petfinder/petfinder-js/dist/petfinder.min.js%22%3E"></script>

<script>
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
            const client = new Client({ apiKey: "HB4E0LPBodtgXJlBVOYvZSDaxgGSCA7Li7Eq6tqb6uVDRfzAp4", secret: "rr6C5OrDLoCg3mP0rk4ztxVTLw3sHwgmvUUMf3zn" });
            client.animal.search()
                .then(function (response) {
                    // Do something with resp.data.animals
                    console.dir(response.data.animals)
                });
        },
        getCats: function () {
          const client = new Client({ apiKey: "HB4E0LPBodtgXJlBVOYvZSDaxgGSCA7Li7Eq6tqb6uVDRfzAp4", secret: "rr6C5OrDLoCg3mP0rk4ztxVTLw3sHwgmvUUMf3zn" });
          var tableOutput = document.getElementById("pfData");
          
          console.log("made it....");

          client.animal.search()
          .then(function (response){
            tableOutput.innerHTML = "";
            for (var i = 0; i < response.data.animals.length; i++ )
            {
              var item = response.data.animals[i];
              if (item.type == 'Cat')
              {
                if (item.photos.length > 0) {
                  var petPic = item.photos[0].medium;
                  tableOutput.innerHTML += "<img src=" + petPic + ">";
                }
                var petName = item.name;
                var petID = item.id;
                var breed = item.breeds.primary;
                var petSize = item.size;
                var petAge = item.age;
                var petDescription = item.description;
                tableOutput.innerHTML += "<h1>" + petName + "</h1>";
                tableOutput.innerHTML += "<h3>Age: " + petAge + "</h3>";
                tableOutput.innerHTML += "<h3>Breed: " + breed + "</h3>";
                tableOutput.innerHTML += "<h3>Size: " + petSize + "</h3>";
                tableOutput.innerHTML += "<h3>" + petDescription + "</h3><br>";
              }
              else
              {
                continue;
              }
            }
          });
      },
        created: function() {
          this.getCats();
          this.getToken();
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
    #pfData {
      font: bold;

    }
</style>