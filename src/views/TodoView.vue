<template>

<div class="home">
  <v-list
  flat
  >
  <div
  v-for="task in tasks"
    :key="task.id"
  >
    <v-list-item>
    <template v-slot:default="{ active,}">
      <v-list-item-action>
        <v-checkbox
          color="primary"
          :input-value="active"
          >
        </v-checkbox>
      </v-list-item-action>

      <v-list-item-content>
        <v-list-item-title>{{ task.title}}</v-list-item-title>
      </v-list-item-content>
      </template>
      
  </v-list-item>
  <v-divider></v-divider>
  </div>
  
</v-list>
  
</div>
</template>

<script>
  export default {
    name: 'TodoView',
   /*  components: {
    }, */
    data() {
      return {
        tasks: [
          {
            id: 1,
            title: 'Wake up'
          },
          {
            id: 2,
            title: 'turn on the computer'
          },
          {
            id: 3,
            title: 'Go to meeting'
          }
        ]
      }
    },

  }
 
    
</script>
