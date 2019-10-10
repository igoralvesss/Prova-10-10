<template>
  <div>
    <v-app-bar
      color="deep-orange darken-2"
      dark
    >

      <v-toolbar-title @click="inicio">Prova Vue.js</v-toolbar-title>

      <div class="flex-grow-1"></div>

      <v-toolbar-title>Igor Alves de Sousa</v-toolbar-title>

      
    </v-app-bar>
  </div>
</template>

<script>
export default {
  data: () => ({
  
  }),
  methods: {
    inicio(){
      this.$router.push('/')
    }
  },
};
</script>
