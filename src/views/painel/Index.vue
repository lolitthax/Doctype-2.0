<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app clipped>
      <!-- lista informações admin -->
      <v-list dense>
        <v-list-item>
          <v-list-item-avatar>
            <v-avatar color="red">
              <span class="white--text headline">AD</span>
            </v-avatar>
          </v-list-item-avatar>
          <v-list-item-title>Jane Smith</v-list-item-title>
        </v-list-item>
        <!-- fim lista -->
        <!-- navegação -->

        <v-list-group value="true">
          <template v-slot:activator>
            <v-list-item-title>Páginas</v-list-item-title>
          </template>

          <v-list-group no-action sub-group value="true">
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>Manutenção</v-list-item-title>
              </v-list-item-content>
            </template>

            <v-list-item v-for="(admin, i) in admins" :key="i" link>
              <v-list-item-title v-text="admin[0]"></v-list-item-title>
              <v-list-item-icon>
                <v-icon v-text="admin[1]"></v-icon>
              </v-list-item-icon>
            </v-list-item>
          </v-list-group>

          <v-list-group sub-group no-action>
            <template v-slot:activator>
              <v-list-item-content>
                <v-list-item-title>Hackathon 2019</v-list-item-title>
              </v-list-item-content>
            </template>
            <v-list-item v-for="(crud, i) in cruds" :key="i">
              <v-list-item-title v-text="crud[0]"></v-list-item-title>
              <v-list-item-action>
                <v-icon v-text="crud[1]"></v-icon>
              </v-list-item-action>
            </v-list-item>
          </v-list-group>
        </v-list-group>
      </v-list>

      <!-- fim navegação -->
    </v-navigation-drawer>

    <!-- barra -->
    <v-app-bar app clipped-left height="100">
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Administração</v-toolbar-title>
      <a href="/">
        <v-icon>mdi-logout</v-icon>
      </a>
      
    </v-app-bar>
    <!-- fim barra -->

    <!-- meio da dash -->
    <v-content>
      <v-container class="fill-height" fluid>
        <v-row align="center" justify="center">
          <v-col class="shrink">
            <v-tooltip right>
              <template v-slot:activator="{ on }">
                <v-btn :href="source" icon large target="_blank" v-on="on">
                  <v-icon large>mdi-code-tags</v-icon>
                </v-btn>
              </template>
              <span>Source</span>
            </v-tooltip>
            <v-tooltip right>
              <template v-slot:activator="{ on }">
                <v-btn
                  icon
                  large
                  href="https://codepen.io/johnjleider/pen/bXNzZL"
                  target="_blank"
                  v-on="on"
                >
                  <v-icon large>mdi-codepen</v-icon>
                </v-btn>
              </template>
              <span>Codepen</span>
            </v-tooltip>
          </v-col>
        </v-row>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  props: {
    source: String
  },
  data: () => ({
    methods: {
      sair(){
        this.$router.push('/');
      },
    },
    admins: [["Início"], ["Preços"], ["Sobre"], ["Contato"]],
    cruds: [["Participantes"]],
    drawer: null
  }),
  created() {
    this.$vuetify.theme.dark = true;
  }
};
</script>