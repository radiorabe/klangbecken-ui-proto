<template>
  <div class="songs">
    <v-layout>
      <v-flex xs2 class="ml-5 mt-3">
        <h1 class="display-1">Songs</h1>
      </v-flex>
      <v-flex xs6 class="mt-3">
        <Search />
      </v-flex>
    </v-layout>
    <v-container>
        <v-layout>
          <v-data-table
            :headers="headers"
            :items="desserts"
            hide-actions
            class="songs-list"
          >
            <template v-slot:items="props">
              <td>{{ props.item.name }}</td>
              <td class="text-xs-left">{{ props.item.calories }}</td>
              <td class="text-xs-left">{{ props.item.fat }}</td>
              <td class="text-xs-right">edit</td>
            </template>
          </v-data-table>
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
            sortable: false,
            value: 'name'
          },
          { text: 'Künstler', value: 'Künstler' },
          { text: 'Dauer', value: 'Dauer' },
          { 
            text: 'Actions',
            align: 'right',
            value: 'Actions' 
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
          }
        ]
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

</style>

<style>

.theme--dark.v-table{
  background-color: transparent;
} 

</style>


