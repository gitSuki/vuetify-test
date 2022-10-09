<script setup>
import { defineEmits } from "vue";

const emits = defineEmits(["selectColorOption"]);

function selectColorOption(isGrayscale) {
  emits("selectColorOption", isGrayscale);
}
</script>

<template>
  <v-navigation-drawer expand-on-hover rail>
    <v-list>
      <v-list-item
        prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
        title="Sandra Adams"
        subtitle="sandra_a88@gmailcom"
      ></v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list density="comfortable" nav>
      <v-list-item
        @click="selectColorOption(false)"
        prepend-icon="mdi-image"
        title="Color Gallery"
        value="color"
      ></v-list-item>
      <v-list-item
        @click="selectColorOption(true)"
        prepend-icon="mdi-dialpad"
        title="Grayspace Gallery"
        value="grayspace"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>
