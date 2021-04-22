<template>
  <div>
    <v-container fluid>
      <v-row>
        <v-navigation-drawer v-model="drawer" absolute temporary>
          <v-row align="align">
            <v-col>
              <v-btn  to="/home"> QUÉ </v-btn>
              <v-btn  to="/home"> DONDE </v-btn>
            </v-col>
          </v-row>
        </v-navigation-drawer>
        <v-app-bar flat fixed>
          <v-app-bar-nav-icon
            class="hidden-md-and-up"
            @click="drawer = !drawer"
          ></v-app-bar-nav-icon>
          <span class="hidden-sm-and-up"></span>
          <v-toolbar-title>
            <router-link to="/" tag="span" style="cursor: pointer">
              {{ appTitle }}
            </router-link>
          </v-toolbar-title>
          <v-spacer></v-spacer>

          <v-toolbar-items class="hidden-sm-and-down">
            <v-row :align="align">
              <v-col
                cols="9"
                :justify="center"
                class="d-flex align-center mb-6"
              >
                <v-btn depressed to="/home"> QUÉ </v-btn>
                <v-btn depressed to="/home"> DONDE </v-btn>
                <div class="text-center">
                  <v-menu offset-y>
                    <template v-slot:activator="{ on, attrs }">
                      <v-btn depressed v-bind="attrs" v-on="on"> CUANDO </v-btn>
                    </template>
                    <v-list>
                      <v-list-item v-for="(item, index) in items" :key="index">
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                      </v-list-item>
                    </v-list>
                  </v-menu>
                </div>

                <v-btn depressed to="/home"> SERVICIOS </v-btn>
              </v-col>
              <v-col cols="12" sm="6" md="3">
                <v-text-field label="Buscar" outlined></v-text-field>
              </v-col>
            </v-row>
          </v-toolbar-items>
        </v-app-bar>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      appTitle: "VISITA RIO CUARTO",
      sidebar: false,
      drawer: false,
      group: null,
      items: [
        { title: "HOY" },
        { title: "MAÑANA" },
        { title: "ESTE FIN DE SEMANA" },
        { title: "ESTE MES" },
        { title: "TODOS" },
      ],
    };
  },
};
</script>