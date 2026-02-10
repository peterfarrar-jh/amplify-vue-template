<script setup lang="ts">
import { Authenticator } from '@aws-amplify/ui-vue';
import '@aws-amplify/ui-vue/styles.css';
import Todos from './components/Todos.vue'

</script>

<template>
  <authenticator>
    <template v-slot="{ user, signOut }">
      <h1>Hello {{ user.signInDetails.loginId }}!</h1>
      <button @click="signOut">Sign Out</button>
        <main>
          <Todos />
        </main>
    </template>
  </authenticator>
</template>

