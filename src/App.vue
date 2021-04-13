<template>
  <v-app>
    <div>
      <Menu />
    </div>
    <v-main>
      <div>
        <v-layout :wrap="true">
          <v-flex xs6> 
            <Card titulo="funcion 1" precio="300"/>
          </v-flex>
          <v-flex xs6> 
            <Card titulo="funcion 2" precio="210"/>
          </v-flex>
        </v-layout>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import Card from "./components/Card";
import Menu from "./components/Menu";

export default {
  name: "App",

  components: {
    Card,
    Menu,
  },

  data: () => ({
    //
  }),
};
</script>
