<script>
export default{
  data(){
    return{
      name:"",
      materia:[]
    }
  }
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
          <label class="input-group-text" for="inputGroupSelect01">Materias</label>
          <select class="form-select" id="inputGroupSelect01" v-model="materia">
           <option selected>...</option>
           <option value="1">Matematica</option>
           <option value="2">Historia</option>
           <option value="3">Ingles</option>
          </select>
        </div>
       <div class="input-group mb-3">
          <span class="input-group-text" id="basic-addon1">Nota</span>
          <input type="text" class="form-control">
        </div>
        <button type="submit" class="btn btn-primary">Añadir</button>
      </div>
      <div class="col-md-8 col-xs-12">
        <h1>Listado</h1>
        <table class="table">
          <tr >
            <th>Nombre</th>
            <th>Materia</th>
            <th>Cualificación</th>
          </tr>
          <tr>
            <th>{{name}}</th>
            <th>{{materia}}</th>
          </tr>
          
        </table>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

</style>
