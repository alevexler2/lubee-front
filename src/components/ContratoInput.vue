<template>
  <div class="d-flex justify-content-center align-items-center">
    <div class="p-4">
      <div class="mb-3">
        <label for="cursoId" class="form-label">ID de Curso:</label>
        <input type="text" id="cursoId" class="form-control" v-model="cursoId" required pattern="\d+">
        <div class="invalid-feedback">Por favor, ingrese un ID de curso válido.</div>
      </div>
      <div class="text-center">
        <button type="submit" class="btn btn-primary" @click="buscarCurso">Buscar</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cursoId: ''
    };
  },
  methods: {
    buscarCurso() {
      this.$emit('buscarContrato', this.cursoId);
    }
  }
};
</script>
