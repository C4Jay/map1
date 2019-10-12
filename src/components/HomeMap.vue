<template>
<v-row align="centre">
    <v-card elevation="21" color="white" width="1229" height="329px">
    <div class="map">
  
                <GmapMap
  v-bind:center="{lat:10, lng:10}"
  v-bind:zoom="7"
  map-type-id="terrain"
  style="width: 1200px; height: 300px"
>
  <GmapMarker
    v-bind:key="index"
    v-for="(m, index) in markers"
    v-bind:position="m.position"
    v-bind:clickable="true"
    v-bind:draggable="true"
    @click="center=m.position"
  />
</GmapMap>

        

    
    </div>
    </v-card>





    <v-card elevation="21" color="white" width="1229" height="329px">
    <div class="map">
  
                <GmapMap
  v-bind:center="{lat:10, lng:10}"
  v-bind:zoom="7"
  map-type-id="terrain"
  style="width: 1200px; height: 300px"
>
  <GmapMarker
    v-bind:key="index"
    v-for="(m, index) in markers"
    v-bind:position="m.position"
    v-bind:clickable="true"
    v-bind:draggable="true"
    @click="center=m.position"
  />
</GmapMap>

        

    
    </div>
    </v-card>

    <v-btn color="green" @click='map'><router-link to="/Maps">Maps</router-link></v-btn>




</v-row>
</template>

<script>
export default {
    name: 'HomeMap',
    data() {
        return {
            center: { lat: 80.0, lng: 80.0 },
            markers: [
                {
                    position: { lat: 7.2563578, lng: 80.6276345 }
                },
                {
                    position: { lat: 7.294544, lng: 80.5907618 }
                }
             
            ]
        };
    },
    methods: {
      login: function() {
        this.$router.replace('about')
      }
    }
    
};
</script>