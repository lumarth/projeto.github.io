<template>
  <v-footer dark padless>
    <v-card flat tile class="lighten-1 white--text text-center bg">
      <v-card-text>
        <v-btn v-for="icon in icons" :key="icon" class="mx-4" icon color="#578A7C">
          <v-icon size="24px" color="#BE9F63">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text
        class="pt-0 texto"
      >Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.</v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text ano">
        {{ new Date().getFullYear() }} —
        <strong>TGM Marcenaria</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
  }),
};
</script>

<style>
.texto {
  color: rgb(87, 86, 86) !important;
}
.bg {
  background-color: #f4eed3 !important;
}

.ano {
  color: rgb(87, 86, 86) !important;
  background-color: #d6c99c;
}
</style>