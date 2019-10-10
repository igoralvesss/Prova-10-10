<template>
  <v-app>
<AppHeader />
  <div class="d-flex justify-center align-center">
    <div class="my-2" @click="notas">
        <v-btn large color="red" class="white--text mt-12">Calcule suas notas</v-btn>
      </div>
  </div>
  </v-app>
</template>

<script>
import AppHeader from '../components/AppHeader';

export default {
  components: {
    AppHeader,
  },
  methods: {
    notas () {
      this.$router.push('/notas')
    },
  }
};
</script>
