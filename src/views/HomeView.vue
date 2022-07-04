<template>
  <v-container fluid fill-height>
    <v-layout align-center justify-center>
      <v-flex xs12 sm8 md5>
        <v-card class="elevation-3">
          <v-toolbar dark color="primary" class="elevation-2" rounded>
            <v-spacer></v-spacer>
            <v-toolbar-title class="text-h4">Posso Misturar ? 🤔</v-toolbar-title>
            <v-spacer></v-spacer>
          </v-toolbar>

          <v-card-text>
            <v-form>
              <v-autocomplete
                dense
                outlined
                solo
                rounded
                :items="items"
              ></v-autocomplete>
              <div class="text-h5 text-center">com</div>
              <div class="transparent--text">.</div>
              <v-autocomplete
                dense
                outlined
                solo
                rounded
                :items="items"
              ></v-autocomplete>
            </v-form>
          </v-card-text>
          <v-card-action>
            <v-dialog v-model="dialog" width="500">
              <template v-slot:activator="{ on, attrs }">
                <v-btn color="primary" class="elevation-2" block v-bind="attrs" v-on="on"
                  >Checar 🔎
                </v-btn>
              </template>

              <v-card>
                <v-card-title class="text-h5 red lighten-2"> 
                  <v-spacer></v-spacer>
                  NÃO !!! 😰
                  <v-spacer></v-spacer> 
                </v-card-title>

                <v-card-text>
                  Ao acrescentar uma substância ácida à água sanitária, vapores
                  tóxicos são produzidos. Eles podem causar sérias queimaduras
                  nos olhos e graves problemas nos pulmões.
                </v-card-text>
              </v-card>
            </v-dialog>
          </v-card-action>
          <!--
          <v-btn color="text-h5 primary" rounded block>Checar</v-btn-->
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      items: ["Água sanitária", "Vinagre", "Água"],
    };
  },
};
</script>

<style></style>
