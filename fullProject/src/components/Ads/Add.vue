<template>
  <v-container>
    <v-layout row>
      <v-flex xs12>
        <v-card>
          <v-card-media :src="ad.imageSrc"></v-card-media>
          <v-card-text>
            <h2 class="orange--text">{{ ad.title }}</h2>
            <p class="text--accent-2">{{ ad.description }}</p>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn class="yellow" flat>Edit</v-btn>
            <v-btn class="amber accent-4">Buy</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  props: ['id'],
  computed: {
    ad () {
      const id = this.id
      return this.$store.getters.adById(id)
    }
  }
}
</script>

<style scoped>

</style>
