<template>
  <v-app>
    <Header />
    <v-content>
      <v-container>
        <router-view></router-view>
      </v-container>
    </v-content>
    <Footer />
  </v-app>
</template>

<script>
import Header from "./components/Header";
import Footer from "./components/Footer";

export default {
  components: { Header, Footer },
};
</script>