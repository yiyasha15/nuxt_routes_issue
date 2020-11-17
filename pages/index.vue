<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <h1>Show list here</h1>
        <v-layout row wrap justify-center >
        <div v-for="users in users" :key ="users.index">
          <v-flex sm6 xs6> 
            <user-card :user="users" ></user-card> 
          </v-flex>
          </div>
    </v-layout>
      </div>
    </v-col>
  </v-row>
</template>

<script>
import axios from 'axios'
import UserCard from '@/components/UserCard.vue'
export default {
    components:{
      UserCard
    },
    async asyncData({error}) {
    try {
      const response = await axios.get('http://localhost:3001/users')
      console.log(response.data);
      return {
        users: response.data
      }
      } catch (e) {
          error({statusCode:503, message: "unable to fetch artist data at this point"})
      }
    },
}
</script>
