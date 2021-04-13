<template> 
  <v-app-bar app color="primary" dark class="space-between" > 
      <div class="d-flex align-center">
        <v-col
        cols="12"
        class="py-2"
      >
      <v-btn>
        VISITA RÌO CUARTO
      </v-btn>
         <v-divider  class="mr-16" vertical inset
    ></v-divider>
    
          <v-btn-toggle
            v-model="text"
            tile
            color="deep-purple accent-3"
            group            
          >
            <v-btn text value="left">
              QUÉ
            </v-btn>

            <v-btn text value="center">
              DÓNDE
            </v-btn>

            <v-btn text value="right">
              CUANDO
            </v-btn>

            <v-btn text value="justify">
              SERVICIOS
            </v-btn>
          </v-btn-toggle>
        
        </v-col>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>
</template>

