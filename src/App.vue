<template>
  <v-app dark>
    <v-content>
      <Home/>
    </v-content>
    <Player />
  </v-app>
</template>

<script>
import Home from '@/views/Home'
import Player from '@/components/Player'


export default {
  name: 'App',
  components: {
    Home,
    Player
  },
  data () {
    return {
      //
    }
  }
}
</script>
