<script setup lang="ts">
import { Authenticator, useAuthenticator } from "@aws-amplify/ui-vue"
import "@aws-amplify/ui-vue/styles.css"

const auth = useAuthenticator()
</script>

<template>
  <div>
    <authenticator>
      <template v-slot="{ user, signOut }">
        <h1>Hello {{ user.username }}!</h1>
        <button @click="signOut">Sign Out</button>
      </template>
    </authenticator>
  </div>
</template>
