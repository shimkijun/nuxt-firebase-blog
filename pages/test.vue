<template>
  <v-container>
    <v-card>
      <v-btn :loading="loading" @click="signIn">
        login
      </v-btn>
      <v-btn :loading="loading" @click="signOut">
        logout
      </v-btn>
    </v-card>
  </v-container>
</template>
<script>
export default {
  data () {
    return {
      items: [],
      loading: false
    }
  },
  methods: {
    async signIn () {
      try {
        this.loading = true
        const provider = new this.$fireAuthObj.GoogleAuthProvider()
        const user = await this.$fireAuth.signInWithPopup(provider)
        console.log(user)
      } catch (e) {
        console.error(e.massage)
      } finally {
        this.loading = false
      }
    },
    async signOut () {
      try {
        this.loading = true
        await this.$fireAuth.signOut()
      } catch (e) {
        console.error(e.massage)
      } finally {
        this.loading = false
      }
    }
  }
}
</script>
