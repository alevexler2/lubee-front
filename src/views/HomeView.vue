<template>
  <div>
    <ContratoInput @buscarContrato="buscarContrato" />
    <ContratoForm v-if="contratoEncontrado" :contrato="contratoEncontrado" />
    <div v-if="error" class="alert alert-danger">{{ error }}</div>
  </div>
</template>

<script>
import axios from 'axios';
import ContratoInput from '../components/ContratoInput.vue';
import ContratoForm from '../components/ContratoForm.vue';

export default {
  components: {
    ContratoInput,
    ContratoForm
  },
  data() {
    return {
      contratoEncontrado: null,
      error: null
    };
  },
  methods: {
    async buscarContrato(contratoId) {
      const idPattern = /^\d+$/;
      if (!idPattern.test(contratoId)) {
        this.error = 'El ID de contrato ingresado no es válido.';
        this.contratoEncontrado = null;
        return;
      }

      try {
        const response = await axios.get(process.env.VUE_APP_API_URL + '/cursos/' + contratoId);
        this.contratoEncontrado = response.data;
        this.error = null;
      } catch (error) {
        this.contratoEncontrado = null;
        this.error = 'No se pudo encontrar el contrato. Por favor, inténtelo nuevamente.';
      }
    }
  }
};
</script>
