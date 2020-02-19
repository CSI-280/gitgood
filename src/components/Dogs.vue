<template>

    <div id="body">
        <div class="container">
          <h1>Find the Dog For You!</h1>
          <h3>
          <p>This box will expand as stuff is added.</p>
          </h3>
        </div>
    </div>
</template>

<script>
    import { Client } from "@petfinder/petfinder-js";

    export default {
        name: 'New',
        data () 
        {
            return {
                msg: 'This is a new page'
            }
        },
        methods: {
            getToken: function () {
                const client = new Client({ apiKey: "HB4E0LPBodtgXJlBVOYvZSDaxgGSCA7Li7Eq6tqb6uVDRfzAp4", secret: "ACCq1YmJ2XzZxT6WrvbSU9voepnbCllw0NmSF363" });

                client.animal.search()
                    .then(function (response) {
                        // Do something with resp.data.animals
                        console.dir(response.data.animals)
                    });
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