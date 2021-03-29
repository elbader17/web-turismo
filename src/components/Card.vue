<template>
  <div>
    <v-layout :wrap="true">
      <v-flex xs12>
        <v-card  class="mx-auto my-12" max-width="374">
          <template slot="progress">
            <v-progress-linear
              color="deep-purple"
              height="10"
              indeterminate
            ></v-progress-linear>
          </template>

          <v-img
            height="250"
            src="https://trucoslondres.com/wp-content/uploads/2017/04/espectaculo.jpg"
          ></v-img>

          <v-card-title>{{ titulo }}</v-card-title>
          <div class="grey--text ml-4">miercoles 7 de abril 21:30</div>
          <v-card-text>
            <!-- <v-row align="center" class="mx-0">
              <v-rating
                :value="4.5"
                color="amber"
                dense
                half-increments
                readonly
                size="14"
              ></v-rating>

              <div class="grey--text ml-4">4.5 (413)</div>
            </v-row> -->

            <div class="my-4 subtitle-1">${{precio}} c/u</div>
            <img />
            <div>Espectaculo teatral</div>
          </v-card-text>

          <v-divider class="mx-4"></v-divider>

          <v-layout :wrap="true">
            <!-- <p class="grey--text ml-4" xs6>aaa</p>
              <img src="./../assets/reloj-contorno-circular.png" height="19" 
              width="19"  xs6> -->
          </v-layout>

          <v-card-text>
            <v-chip-group
              active-class="deep-purple accent-4 white--text"
              column
            >
              <v-chip>Teatro</v-chip>

              <v-chip>Festival</v-chip>

              <v-chip>Musica</v-chip>
            </v-chip-group>
            <p>En el teatro municipal</p>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  data: () => ({
   //
  }),
  props:['titulo', 'precio']
};
</script>