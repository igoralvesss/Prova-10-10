<template>
    <div>
        <AppHeader />
        <div class="d-flex justify-center align-center mt-12">
            <v-card
    max-width="600px"
    height="250px"
    class="mx-auto"
  >
     <v-form v-model="valid">
    <v-container>
      <v-row class="alinhamento">
        <v-col
          cols="12"
          md="4"
          
        >
          <v-text-field
            v-model="primeiranota"
            :rules="notaRules"
            :counter="2"
            label="Nota 1"
            required
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          md="4"
          class="ml-10"
        >
          <v-text-field
            v-model="segundanota"
            :rules="notaRules"
            :counter="2"
            label="Nota 2 "
            required
          ></v-text-field>
        </v-col>
      </v-row>
    <div class="botoes">
        <v-btn
      :disabled="!valid"
      color="success"
      class="mt-10 ml-n5 "
      @click="validate"
    >
      Calcular Média
    </v-btn>

    <div class="ml-5 mt-10">
        <v-btn text large> R: {{ resultado }}</v-btn>
      </div>
    </div>
      
    </v-container>
  </v-form>
  </v-card>
        </div>
    </div>
</template>

<style>

.alinhamento{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}

.botoes{
    display: flex;
    align-items: center;
    justify-content: center;
}

</style>

<script>
import AppHeader from '../components/AppHeader';

export default {
  components: {
    AppHeader,
  },
  data: () => ({
      valid: true,
      primeiranota: '',
      var: n1,
      notaRules: [
        v => !!v || 'Nota é obrigatória',
        v => (v && v.length <= 2) || 'Nota só pode conter 2 números',
      ],
      segundanota: '',
      var: n2,
      notaRules: [
        v => !!v || 'Nota é obrigatória',
        v => (v && v.length <= 2) || 'Nota só pode conter 2 números',
      ],
    }),
    methods: {
      validate () {
        if (this.$refs.form.validate()) {
          this.snackbar = true
        }
      },
    
}
}
</script>