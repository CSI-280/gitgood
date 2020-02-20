<template onload="created()">

    <div id="body">
        <div class="container">
          <h1>Find the Dog For You!</h1>
          <h3>
          <p>This box will expand as stuff is added.</p>
          </h3>
          <table>
              <thead>
                    <tr>
                        <td>Name</td>
                        <td>Id</td>
                        <td>Primary Breed</td>
                        <td>Size</td>
                        <td>Age</td>
                    </tr>
              </thead>
              <tbody id="dogTable">   

              </tbody>
          </table>
        </div>
        <button id="dogButton" v-on:click='getDogs()'>click me</button>
    </div>
</template>

<script>
    import { Client } from "@petfinder/petfinder-js";
    import { Animal } from "@petfinder/petfinder-js/dist/api/animal";

    export default {
        name: 'Dogs',
        data () 
        {
            return {
                msg: 'This is the dogs page'
            }
        },
        methods: {
            getDogs: function () {
                const client = new Client({ apiKey: "HB4E0LPBodtgXJlBVOYvZSDaxgGSCA7Li7Eq6tqb6uVDRfzAp4", secret: "rr6C5OrDLoCg3mP0rk4ztxVTLw3sHwgmvUUMf3zn" });
                client.animal.search().then(function (response) {
                    //console.dir(response.data.animals);
                    var table = document.getElementById('dogTable');
                    var data = '';
                    table.innerHTML = '';


                    for (var i = 0; i < response.data.animals.length; i++ )
                    {     
                        var animal = response.data.animals[i];  
                        if(animal.type == 'Dog') {
                            data += '<tr>';
                            data += '<td>' + animal.name + '</td>';
                            data += '<td>' + animal.id + '</td>';
                            data += '<td>' + animal.breeds.primary + '</td>';
                            data += '<td>' + animal.size + '</td>';
                            data += '<td>' + animal.age + '</td>';
                            
                            data += '</tr>';

                            table.innerHTML += data;
                            data = '';
                        }
                    }
                });
            },
            created: function() {
            this.getDogs();
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

    #dogTable {  
    color: #333; /* Lighten up font color */
    font-family: Helvetica, Arial, sans-serif;
    width: auto;
    min-width: 640px;
    border-spacing: 0ch;
    vertical-align: middle;
    text-align: center;
    }

    th {  
        background: rgba(243, 243, 243, 0.603);
        font-weight: bold;
        border: 1px solid rgba(204, 204, 204, 0.137);
        height: 30px;
    }
    
    td {  
        background: #FAFAFA; /* Lighter grey background */
        text-align: center; /* Center our text */
        border: 1px solid #CCC;
        height: 30px;
    }
</style>