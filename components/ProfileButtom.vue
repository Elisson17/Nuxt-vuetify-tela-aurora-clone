<template>
  <v-menu>
    <template v-slot:activator="{ props }">
      <v-btn
      style="font-size: 12px;"
        v-bind="props"
        prepend-icon="mdi-account"
        append-icon="mdi-chevron-down"
      >
        Elisson Silva</v-btn
      >
    </template>
    <v-list>
      <v-list-item>
        <v-list-item-title> botão imaginario </v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script setup></script>

<style scoped>

</style>
