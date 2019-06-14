<template>
  <v-navigation-drawer stateless app :value="drawer" class="nav">
    <v-layout align-space-between justify-center column>
      <v-flex>
        <div class="logo text-xs-center mt-5">
          <img src="@/assets/logo.svg" alt="RaBe Logo">
        </div>
      </v-flex>
      <v-flex class="mt-1"> 
        <v-list class="mt-1">
          <div 
            v-for="row in navContent"
            :key="row.name" 
          >
            <v-list-tile class="mx-4 my-5 bullet">
              <v-list-tile-action>
                <v-icon class="white--text">{{ row.icon }}</v-icon>
              </v-list-tile-action>
              <v-list-tile-content>
                <v-list-tile-title class="white--text">{{ row.name }}</v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>
          </div>
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
        { name: "Music", icon: "music_note" },
        { name: "Jingles", icon: "notifications" }
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
.nav{
}

.bullet:hover{
  background-color: rgba(0, 0, 0, 0.5);
  cursor: pointer;
}
</style>
