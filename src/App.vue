<template>
  <v-app class="app-color">
    <v-main class="main">
      <LoginComponent />
    </v-main>

    <FooterComponent />
  </v-app>
</template>

<script>
import LoginComponent from './components/LoginComponent';
import FooterComponent from './components/layout/FooterComponent';

export default {
  name: 'App',

  components: {
    LoginComponent,
    FooterComponent
  },

  data: () => ({
    //
  }),
};
</script>

<style>
.app-color {
  background-color:#252537 !important;
}

.main {
  padding: 0px 0px 0px;
}

</style>