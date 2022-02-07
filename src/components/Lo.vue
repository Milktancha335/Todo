<template>
  <v-container>
    <v-card
      class="mx-auto"
      max-width="720"
      v-for="(item, index) in A1"
      :key="index"
      height="100"
    >
      <v-list-item-content>
        <center>
          <v-list-item-subtitle>
            {{ item.name }}
          </v-list-item-subtitle>
        </center>
        <br />
      </v-list-item-content>
       <v-btn
          class="mx-2 "
          fab
          dark
          small
          color="bg-danger"
          @click="deleteTodo(index)"
          ><v-icon dark>mdi-minus</v-icon>
        </v-btn>
    </v-card>
  </v-container>
</template>

<script>
export default {
  props: ["A1"],
  methods: {
    deleteTodo(index) {
      this.A1.splice(index, 1);
    },
  },
};
</script>

<style>
</style>
//Excel