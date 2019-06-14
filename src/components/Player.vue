<template>
  <v-toolbar class="player" height="80">
    <v-toolbar-side-icon @click="toggleDrawer"></v-toolbar-side-icon>
  </v-toolbar>
</template>

<script>
export default {
  name: "Player",
  data() {
    return {

    }
  },
  methods: {
    toggleDrawer(){
      this.$store.commit('toggleDrawer')
    }
  },
}
</script>

<style scoped>
.player{
  position: absolute;
  bottom: 0;
  z-index: 3;
  background-color: rgba(0, 0, 0, 0.5)
}
</style>





