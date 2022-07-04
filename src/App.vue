<template>
  <v-app>
    <v-app-bar app color="primary" elevation="1"
      ><!--barra superior-->
      <v-app-bar-nav-icon></v-app-bar-nav-icon
      ><!--hamburguer
      <v-switch
        v-model="$vuetify.theme.dark"
        inset
        persistent-hint
      ></v-switch>-->
    </v-app-bar>

    <v-main class="grey lighten-4">
      <router-view></router-view>
    </v-main>

    <v-footer app
      ><span class="caption">Posso Misturar &copy; 2022</span></v-footer
    >
  </v-app>
</template>

<script>
export default {};
</script>

<style></style>
