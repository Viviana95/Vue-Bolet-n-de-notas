<script>
import DataTable from "../components/DataTable.vue";

export default{
    data() {
        return {
            name: "",
            materia: "",
        };
    },
    components: { DataTable }
}
</script>
<template>
  <div class="container">
    <div class="row">
      <div class="col-md-4 col-xs-12">
        <h1>Agregar alumno</h1>
        <div class="input-group mb-3">
          <span class="input-group-text" id="basic-addon1">Nombre</span>
          <input type="text" class="form-control" v-model="name">
        </div>
        <div class="input-group mb-3">
          <span class="input-group-text" id="basic-addon1">Materia</span>
          <input type="text" class="form-control">
        </div>
       <div class="input-group mb-3">
          <span class="input-group-text" id="basic-addon1">Nota</span>
          <input type="text" class="form-control">
        </div>
        <button type="submit" class="btn btn-primary">Añadir</button>
      </div>
      <DataTable/>
      
    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>
