<script setup>
import { defineProps, computed } from 'vue'

const props = defineProps(['isGrayscale'])
const grayScaleQuery = computed(() => props.isGrayscale ? "&grayscale" : "")
</script>

<template>
  <v-card class="mx-5 my-3 pa-3">
    <v-row>
      <v-col v-for="n in 200" :key="n" cols="4" sm="2">
        <v-card></v-card>
        <v-img
          :src="`https://picsum.photos/500/300?image=${n * 5 + 10}${grayScaleQuery}`"
          :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}${grayScaleQuery}`"
          aspect-ratio="1"
          cover
        >
          <template v-slot:placeholder>
            <v-row class="fill-height ma-0" align="center" justify="center">
              <v-progress-circular
                indeterminate
                color="grey-lighten-5"
              ></v-progress-circular
            ></v-row>
          </template>
        </v-img>
      </v-col>
    </v-row>
  </v-card>
</template>
