<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Vuetify</span>
        <span class="font-weight-light">MATERIAL DESIGN</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <v-row align="center">
      <home-map></home-map>
      <home-map1></home-map1>

      </v-row>
    </v-content>
  </v-app>
</template>

<script>
import HomeMap from '@/components/HomeMap.vue';
import HomeMap1 from '@/components/HomeMap1.vue';

export default {
  name: 'App',
  components: {
    HomeMap,
    HomeMap1
  },
  data: () => ({
    //
  }),
};
</script>
