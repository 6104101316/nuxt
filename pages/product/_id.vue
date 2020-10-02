<template>
  <div>
    <v-row>
      <v-col md="4" />
      <v-col md="4" align="center" justify="center">
        <h1>{{ id.trackName }}</h1>
        <br>
        <v-img :src="id.artworkUrl100" max-height="300" max-width="300" />
      </v-col>
      <v-col md="4" />
    </v-row>
    <v-col align="center" justify="center">
      <h3>{{ id.artistName }}</h3>
      <h3>CollectionName : {{ id.collectionName }}</h3>
      <br>
      <audio controls>
        <source :src="id.previewUrl" type="audio/mpeg">
      </audio>
      <a
        style="text-decoration: none;"
        target="_blank"
        :href="id.trackViewUrl"
      />
    </v-col>

    <div class="text-center">
      <v-btn :href="id.trackViewUrl">
        GO SOME WHERE
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      id: this.$route.params.id
    }
  }
}
</script>

<style></style>
