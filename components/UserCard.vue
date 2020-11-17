<template>
<v-hover>
  <template v-slot="{ hover }" >
  <v-card class = "ma-1 pa-1 lighten-5" :elevation="hover ? 6 : 1" :to="'/' + user.id" min-width="180" max-height="260"> <!-- dark -->
    <v-container align="center">
            <p >
            {{ user.username }}
            </p>
    </v-container>
  </v-card>
  </template>
</v-hover>
</template>

<script>
    export default {
      name: 'UserCard',
      props: {
        user: Object
      },
      }
</script>

