<template>
    <v-app>
        <div>
            <nuxt-child :user="user"/>
        </div>
        <h1 class="my-6">Hi</h1>
        <div>
            <v-btn dark rounded color="primary" :to= "`/${user.id}/`">name</v-btn>
            <v-btn dark rounded color="primary" :to= "`/${user.id}/work`"> Work </v-btn>
        </div>
        <h1 class="my-6">
            this is username page.
            my name is {{user.username}}.
        </h1>
    </v-app>
</template>
<script>
export default {
    async asyncData({ params, $axios }) {
      const user = await $axios.$get(`http://localhost:3001/users/${params.id}`)
      console.log(user);
      return { user }
    }
    // async asyncData({error, params}) {
    // try {
    //   const response = await axios.get('http://localhost:3001/users/${params.id}')
    //   console.log(response.data);
    //   return {
    //     user: response.data
    //   }
    //   } catch (e) {
    //       error({statusCode:503, message: "unable to fetch artist data at this point"})
    //   }
    // },
    // props: {
    //     user: Object
    //   },
}
</script>