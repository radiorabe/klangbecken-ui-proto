<template>
  <div class="songs white--text">
    <v-container class="songs-wrapper">
      <v-layout align-center justify-start row wrap>
        <v-flex xs2>
          <h1 class="display-2 font-weight-light">Music</h1>
        </v-flex>
        <v-flex xs8>
          <Search :list="desserts"/>
        </v-flex>
        <v-flex xs2>
          <v-btn class="btn-logout font-weight-light grey--text flat right">Logout</v-btn>
        </v-flex>
      </v-layout>
      <v-layout column class="mt-4">
          <v-flex>
              <v-card 
                flat 
                class="pa-2 font-weight-light subheading song-item transparent white--text"
              >
                <v-layout>
                  <v-flex xs4>
                    <div>Artist</div>
                  </v-flex>
                  <v-flex xs5>
                    <div class="text-xs-left">Title</div>
                  </v-flex>
                  <v-flex xs1>
                    <div class="text-xs-left">Length</div>
                  </v-flex>
                  <v-flex xs2>
                    <div></div>
                  </v-flex>
                </v-layout>
              </v-card>
          </v-flex>
          <v-divider class="thead-divider"></v-divider>
        <div class="scroll-box">
          <v-flex>
            <div 
              v-for="item in desserts" 
              :key="item.calories"
            >
              <v-card 
                flat 
                class="pa-2 font-weight-light subheading song-item transparent white--text"
              >
                <v-layout class="song-hover">
                  <v-flex xs4>
                    <div>{{ item.name }}</div>
                  </v-flex>
                  <v-flex xs5>
                    <div class="text-xs-left">{{ item.calories }}</div>
                  </v-flex>
                  <v-flex xs1>
                    <div class="text-xs-left">{{ item.fat }}</div>
                  </v-flex>
                  <v-flex xs2 class="toggle-visibility">
                    <div class="text-xs-center">
                      <v-layout justify-center>
                          <v-icon small color="white">edit</v-icon>
                          <v-icon small class="mx-3 white--text">add</v-icon>
                          <v-icon small color="white">delete</v-icon>
                      </v-layout>
                    </div>
                  </v-flex>
                </v-layout>
              </v-card>
            </div>
          </v-flex>
        </div>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
import Search from '@/components/Search.vue'

  export default {
    name: "Songs",
    components: {
      Search
    },
    data () {
      return {
        headers: [
          {
            text: 'Title',
            align: 'left',
            value: 'name',
            sortable: false,
          },
          { 
            text: 'Künstler', 
            value: 'Künstler',
            sortable: false, 
          },
          { 
            text: 'Dauer', 
            value: 'Dauer',
            sortable: false, 
          },
          { 
            text: 'Actions',
            align: 'right',
            value: 'Actions',
            sortable: false,
          }
        ],
        desserts: [
          {
            name: 'Frozen Yogurt',
            calories: 159,
            fat: 6.0,
            carbs: 24,
            protein: 4.0,
            iron: '1%'
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
            fat: 9.0,
            carbs: 37,
            protein: 4.3,
            iron: '1%'
          },
          {
            name: 'Eclair',
            calories: 262,
            fat: 16.0,
            carbs: 23,
            protein: 6.0,
            iron: '7%'
          },
          {
            name: 'Cupcake',
            calories: 305,
            fat: 3.7,
            carbs: 67,
            protein: 4.3,
            iron: '8%'
          },
          {
            name: 'Gingerbread',
            calories: 356,
            fat: 16.0,
            carbs: 49,
            protein: 3.9,
            iron: '16%'
          },
          {
            name: 'Jelly bean',
            calories: 375,
            fat: 0.0,
            carbs: 94,
            protein: 0.0,
            iron: '0%'
          },
          {
            name: 'Lollipop',
            calories: 392,
            fat: 0.2,
            carbs: 98,
            protein: 0,
            iron: '2%'
          },
          {
            name: 'Honeycomb',
            calories: 408,
            fat: 3.2,
            carbs: 87,
            protein: 6.5,
            iron: '45%'
          },
          {
            name: 'Donut',
            calories: 452,
            fat: 25.0,
            carbs: 51,
            protein: 4.9,
            iron: '22%'
          },
          {
            name: 'KitKat',
            calories: 518,
            fat: 26.0,
            carbs: 65,
            protein: 7,
            iron: '6%'
          },
          {
            name: 'Frozen Yogurt',
            calories: 159,
            fat: 6.0,
            carbs: 24,
            protein: 4.0,
            iron: '1%'
          },
          {
            name: 'Ice cream sandwich',
            calories: 237,
            fat: 9.0,
            carbs: 37,
            protein: 4.3,
            iron: '1%'
          },
          {
            name: 'Eclair',
            calories: 262,
            fat: 16.0,
            carbs: 23,
            protein: 6.0,
            iron: '7%'
          },
          {
            name: 'Cupcake',
            calories: 305,
            fat: 3.7,
            carbs: 67,
            protein: 4.3,
            iron: '8%'
          },
          {
            name: 'Gingerbread',
            calories: 356,
            fat: 16.0,
            carbs: 49,
            protein: 3.9,
            iron: '16%'
          },
          {
            name: 'Jelly bean',
            calories: 375,
            fat: 0.0,
            carbs: 94,
            protein: 0.0,
            iron: '0%'
          },
          {
            name: 'Lollipop',
            calories: 392,
            fat: 0.2,
            carbs: 98,
            protein: 0,
            iron: '2%'
          },
          {
            name: 'Honeycomb',
            calories: 408,
            fat: 3.2,
            carbs: 87,
            protein: 6.5,
            iron: '45%'
          },
          {
            name: 'Donut',
            calories: 452,
            fat: 25.0,
            carbs: 51,
            protein: 4.9,
            iron: '22%'
          },
          {
            name: 'KitKat',
            calories: 518,
            fat: 26.0,
            carbs: 65,
            protein: 7,
            iron: '6%'
          }
        ]
      }
    },
    computed: {
      test() {
        let one = document.getElementsByClassName('song-item')
        let two = document.getElementsByClassName('toggle-visibility')
          
        one.addEventListener('mouseover', function(){
          two.style.opacity = 1
          one.style.backgroundColor = "red"
        }, true)
        one.addEventListener('mouseout', function(){
          two.style.opacity = 0
          one.style.backgroundColor = "transparent"
        }, true)

        return true
      }
    }
  }
</script>

<style scoped>
.songs{
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
}

.songs-list{
  width: 100%;
}

.songs-wrapper{
  max-width: 1337px;
}

.song-item{
  border-radius: 0px;
}

.toggle-visibility{
  visibility: visible;
}

.transparent{
  background-color: transparent;
}

.scroll-box{
  overflow-x: hidden;
  overflow-y: scroll;
  height: 72vh;
}

.thead-divider{
  border-color: white;
}

.btn-logout{
  border-radius: 15px;
  border: 1px solid #444;
  background-color: transparent !important;
  height: 30px;
}

::-webkit-scrollbar {
  width: 4px;
}

::-webkit-scrollbar-track {
  background: #444;
}
 
::-webkit-scrollbar-thumb {
  background: #f1f1f1; 
  border-radius: 10px;
}

::-webkit-scrollbar-thumb:hover {
  background: #555; 
}
</style>


