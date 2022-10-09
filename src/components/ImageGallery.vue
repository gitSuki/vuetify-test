<template>
  <v-row>
    <v-col v-for="n in 200" :key="n" cols="2">
      <v-card></v-card>
      <v-img
        :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
        aspect-ratio="1"
        cover
      ></v-img>
    </v-col>
  </v-row>
</template>
