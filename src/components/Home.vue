<template>
  <v-content>
    <v-card class="mx-auto" max-width="100%">
      <v-img
        class="white--text align-end"
        height="400px"
        src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
      ></v-img>
      <v-card-subtitle class="pb-0">TGM Marcenaria</v-card-subtitle>

      <v-card-text class="text--primary" font-size="25px">
        <div>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim eaque, unde amet minus eius dolorem a? Ut et qui explicabo totam! Blanditiis nobis quos vel autem. Magni sapiente officiis est!</div>
      </v-card-text>
    </v-card>

    <br />
    <v-sheet class="mx-auto" elevation="8" max-width="100%">
      <v-row class="título">
        <h3 class="title">Nossos últimos trabalhos</h3>
      </v-row>
      <v-slide-group v-model="model" class="pa-4" show-arrows>
        <v-slide-item v-for="n in 15" :key="n" v-slot:default="{ active, toggle }">
          <v-card
            :color="active ? 'primary' : 'grey lighten-1'"
            class="ma-4"
            height="400"
            width="200"
            @click="toggle"
          >
            <v-row class="fill-height" align="center" justify="center">
              <v-scale-transition>
                <v-icon v-if="active" color="white" size="48" v-text="'mdi-close-circle-outline'"></v-icon>
              </v-scale-transition>
            </v-row>
          </v-card>
        </v-slide-item>
      </v-slide-group>

      <v-expand-transition>
        <v-sheet v-if="model != null" color="grey lighten-4" height="200" tile>
          <v-row class="fill-height" align="center" justify="center">
            <h3 class="title">Selected {{ model }}</h3>
          </v-row>
        </v-sheet>
      </v-expand-transition>
    </v-sheet>
    <br />
  </v-content>
</template>

<script>
export default {
  data: () => ({
    model: null,
  }),
};
</script>

<style>
.título {
  padding-top: 1rem;
  margin-left: 1.5rem;
}
.título1 {
  display: absolute;
  margin-left: 1.5rem;
  margin-top: 1rem;
}
.pb-0 {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 0.6rem;
  margin-top: 1rem;
}
.text--primary {
  font-size: 1.1rem;
}
</style>