<template>
  <div class="d-flex justify-content-center align-items-center">
    <form class="p-4 w-50">
      <div class="mb-3">
        <label>Código de curso:</label>
        <input type="text" v-model="contrato.Contrato.CourseCode" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Fecha de alta:</label>
        <input type="text" v-model="formattedCreateDate" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Colegio:</label>
        <input type="text" v-model="contrato.Contrato.ColegioNombre" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Nivel:</label>
        <input type="text" v-model="contrato.Contrato.ColegioNivel" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Curso:</label>
        <input type="text" v-model="contrato.Contrato.ColegioCurso" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Localidad:</label>
        <input type="text" v-model="contrato.Contrato.ColegioLocalidad" readonly class="form-control">
      </div>
      <h3>Pedido</h3>
      <div class="mb-3">
        <label>Cantidad:</label>
        <input type="text" v-model="contrato.Contrato.CantidadEgresados" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Artículo:</label>
        <input type="text" v-model="contrato.Producto.Nombre" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Precio unitario:</label>
        <input type="text" v-model="contrato.Producto.Precio" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Total:</label>
        <input type="text" v-model="contrato.Contrato.Total" readonly class="form-control">
      </div>
      <div class="mb-3">
        <label>Fecha de entrega:</label>
        <input type="text" v-model="formattedFechaEntrega" readonly class="form-control">
      </div>
    </form>
  </div>
</template>

<script>
import { format } from 'date-fns';

export default {
  props: {
    contrato: {
      type: Object,
      required: true
    }
  },
  computed: {
    formattedCreateDate() {
      const createDate = new Date(this.contrato.CreateDate);
      return format(createDate, 'yyyy-MM-dd');
    },
    formattedFechaEntrega() {
      const fechaEntrega = new Date(this.contrato.Contrato.FechaEntrega);
      return format(fechaEntrega, 'yyyy-MM-dd');
    }
  }
};
</script>
