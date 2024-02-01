<template>
  <div class="about">
    <v-list-item max-width="800" v-for="u in utenti" :key="u.id" :title="u.firstName" :subtitle="u.lastName">
      <template v-slot:prepend>
        <v-avatar :image=u.image></v-avatar>
      </template>
      <template v-slot:append>
        <v-btn  @click=""  color="grey-lighten-1" icon="mdi-information" variant="text"></v-btn>
      </template>
    </v-list-item>
   
  </div>
</template>

<script>
import ut from "../utenti";
export default {
  name: 'HomeView',
  data() {
    return {
      utenti: [],
    };
  },
  created() {
    this.utenti = ut;
  },
};
</script>
