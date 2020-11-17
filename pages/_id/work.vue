<template>
    <!-- <v-app> -->
        <div>
        <h1 class="my-6">Hello</h1>
        <div>
            <v-btn dark rounded color="primary" :to= "`/${user.id}/`">name</v-btn>
            <v-btn dark rounded color="primary" :to= "`/${user.id}/work`"> Work </v-btn>
        </div>
        <h1 class="my-6">
            this is work page. 
            my name is {{user.username}}.
        </h1>
        </div>
    <!-- </v-app> -->
</template>
<script>
export default {
    props: {
        user: Object
      },
}
</script>