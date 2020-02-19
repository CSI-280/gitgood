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

            <div class="bold">
                <p>Let Us Help You Find the Perfect Animal...</p>
            </div>
            <hr width=80%>
            <div class = "pet-row">
                <div class="left-img">
                    <div class="image-wrapper">
                        <img src="../assets/mastiff.jpg">
                    </div>
                </div>
                <div class="text">
                    <p>Big or Small...</p>
                </div>
                <div class="right-img">
                    <div class="image-wrapper">
                        <img src="../assets/yorkie.png">
                    </div>
                </div>
            </div>
            <div class = "pet-row">
                <div class="left-img">
                    <div class="image-wrapper">
                        <img src="../assets/golden.png">
                    </div>
                </div>
                <div class="text">
                    <p>Canine or Feline...</p>
                </div>
                <div class="right-img">
                    <div class="image-wrapper">
                        <img src="../assets/cat.png">
                    </div>
                </div>
            </div>
            <div class = "pet-row">
                <div class="left-img">
                    <div class="image-wrapper">
                        <img src="../assets/hairydog.jpg">
                    </div>
                </div>
                <div class="text">
                    <p>Furry or... Not</p>
                </div>
                <div class="right-img">
                    <div class="image-wrapper">
                        <img src="../assets/hairlesscat.jpg">
                    </div>
                </div>
            </div>
            <div class="bold">
                <p>We've Got You Covered!</p>
            </div>
            <hr width=80%>
            <div class="bold">
                <p>Contact Us:</p>
            </div>
            <div class="contact-info">
                <p>git-a-pet LLC</p>
                <p>(802) 867 5309 </p>
                <p>git-a-pet@mymail.champlain.edu</p>
                <p>375 Maple St. Burlington, VT 05401</p>
                <p>Joyce Hall Room 210</p>
                <p>Mondays & Wednesdays 5:00 - 6:15pm</p>
            </div>
            <div id="map"></div>
      </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .bold {
        text-align: center;
        font-weight: bold;
        font-size: 35pt;
    }

    .pet-row {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 69vw;
        height: 25vh;
    }

    .left-img {
        float: left;
    }

    .text {

        text-align: center;
        vertical-align: middle;
        font-size: 30pt;
        margin-left: 2vw;
        margin-right: 2vw;
    }

    .right-img {

        float: right;
    }

    img {
        width: auto;
        height: 10vw;
        border-radius: 2em 2em 2em 2em;
        float: left;
    }

    .contact-info {
        margin-left: 10vw;
        text-align: left;
        font-size: 16pt;
    }

    #map {
        height: 10vh;
        width: auto;  
        float: right;
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


