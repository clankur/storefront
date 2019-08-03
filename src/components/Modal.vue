<template>
  <div class="text-center">
    <v-dialog v-model="dialog" width="500">
      <template v-slot:activator="{ on }">
        <v-btn color="blue lighten-2" dark v-on="on">{{modalData.enablerText}}</v-btn>
      </template>

      <v-card>
        <v-toolbar>
          <v-btn icon dark @click="dialog = false">
            <v-icon>close</v-icon>
          </v-btn>
          <v-card-title primary-title>
            <h3>{{modalData.title}}</h3>
          </v-card-title>
        </v-toolbar>

        <v-card-text>{{modalData.text}}</v-card-text>

        <v-divider></v-divider>

        <v-card-actions v-if="modalData.buttons">
          <v-spacer></v-spacer>
          <v-btn color="primary" text @click="dialog = false">I accept</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script lang="js">
export default {
  name: "Modal",
  props: ["modalData"],
  
  data() {
    return {
      dialog: false
    };
  }
};
</script>
