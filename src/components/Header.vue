<template>
  <div>
    <v-toolbar>
      <v-app-bar absolute color="#f4eed3" dark>
        <v-app-bar-nav-icon class="nave" color="#6d9888" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

        <v-toolbar-title class="headline font-weight tt">TGM Marcenaria</v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn icon color="#6d9888">
          <v-icon color="#6d9888">mdi-magnify</v-icon>
        </v-btn>
      </v-app-bar>
    </v-toolbar>
    <v-navigation-drawer open-on-hover v-model="drawer" absolute temporary>
      <v-list-item>
        <v-list-item-avatar></v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>Navegação</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-btn text block to="/">Home</v-btn>
        <v-btn text block to="/quem-somos">Quem Somos</v-btn>
        <v-btn text block>Serviços</v-btn>
        <v-btn text block to="/contato">Contato</v-btn>

        <v-list-item>
          <v-list-item-content></v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      drawer: null,
      items: [
        { title: "Home" },
        { title: "Quem Somos" },
        { title: "Serviços" },
        { title: "Contato" },
      ],
    };
  },
};
</script>

<style>
.bt {
  background-color: #ffffff !important;
  height: 2rem;
}
.tt {
  color: #be9f63;
  font-weight: 600;
  font-family: unquote("Open Sans");
  font-size: 95px;
}
</style>