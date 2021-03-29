<template>
    <div>
        <v-layout :wrap="true">
            <v-flex xs12>
                <v-card
    :loading="loading"
    class="mx-auto my-12"
    max-width="374"
  >
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

    <v-card-title>Teatro municipal</v-card-title>

    <v-card-text>
      <v-row
        align="center"
        class="mx-0"
      >
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ml-4">
          4.5 (413)
        </div>
      </v-row>

      <div class="my-4 subtitle-1">
        $400 c/u
      </div>

      <div>Espectaculo teatral</div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>Horarios</v-card-title>

    <v-card-text>
      <v-chip-group
        active-class="deep-purple accent-4 white--text"
        column
      >
        <v-chip>5:30PM</v-chip>

        <v-chip>7:30PM</v-chip>

        <v-chip>8:00PM</v-chip>

        <v-chip>9:00PM</v-chip>
      </v-chip-group>
    </v-card-text>
  </v-card>

            </v-flex>
            
        </v-layout>



    </div>
</template>