<template>
  <v-app>
    <v-main>
      <v-btn @click="dialogs.user = true">Show User</v-btn>
      <user-dialog v-model="dialogs.user" @close="dialogs.user = false"></user-dialog>
    </v-main>
  </v-app>
</template>

<script>
  import UserDialog from '@/components/UserDialog'

  export default {
    name: 'App',
    components: {
      UserDialog
    },
    data() {
      return {
        dialogs: {
          user: false,
        }
      }
    }
  }
</script>
