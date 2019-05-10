<template>
    <v-navigation-drawer stateless app :value="drawer" class="nav">
  
    <v-layout align-space-between justify-center column>
      <v-flex>
    <div class="logo text-xs-center mt-3">
      <img src="@/assets/logo.svg" alt="RaBe Logo">
    </div>
    </v-flex>
      <v-flex class="mt-5"> 
        <v-list class="mt-5">
          <v-list-tile 
            v-for="row in navContent" 
            :key="row.name" 
            class="mx-4 my-5"
          >
            <v-list-tile-action>
              <v-icon>{{ row.icon }}</v-icon>
            </v-list-tile-action>

            <v-list-tile-content>
              <v-list-tile-title>{{ row.name }}</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-flex>
    </v-layout>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "Navigation",
  data () {
    return {
      navContent: [
        { name: "Songs", icon: "music_note" },
        { name: "Jingles", icon: "music_note" },
        { name: "Playlist", icon: "music_note" },
      ],
    }
  },
  methods: {

  },
  computed: {
    drawer() {
      return this.$store.state.drawer
    }
  }
}
</script>

<style scoped>
</style>
