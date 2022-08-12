<script>
import DataTable from './DataTable.vue';


export default {
  data() {
    return {
      students: [],
      name: "",
      signature: "",
     // note: "",
      id: "",
      

    };
  },
  methods: {
    selectSignature(){
      this.signature = ref("")
    },

    notas(){
      //if(this.note == 5){return "Suspenso"};
       //return this.note === 5 ? "ok":"mal";
    },

    addStudent() {
      if (this.name.length === 0) { return };
      if (this.signature.length === 0) { return };
      if (this.note.length === 0) { return };
      id: this.students.length + 1,
        this.students.push({
          //id:this.id++,
          id: this.students.length + 1,
          name: this.name,
          signature: this.signature,
          note: this.note,
        });
      this.name = "";
      this.note = "";
      this.signature = "";
      
    },
    
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
          <label class="input-group-text" for="inputGroupSelect01">Options</label>
          <select class="form-select" id="inputGroupSelect01" v-model="signature">
            <option selected>Choose...</option>
            <option value="Matemáticas">Matemáticas</option>
            <option value="Español">Español</option>
            <option value="Historia">Historia</option>
          </select>
        </div>
        
        <div class="input-group mb-3">
          <span class="input-group-text" id="basic-addon1">Nota</span>
          <input type="text" class="form-control" v-model="note">
        </div>
        <button @click="addStudent()" type="submit" class="btn btn-primary">Añadir</button>
      </div>
      <div class="col-md-8 col-xs-12">
        <h1>Listado</h1>
        <table class="table">
          <tr>
            <th>Nombre</th>
            <th>Materia</th>
            <th>Cualificación</th>
          </tr>
          <tr v-for="(student, key) in students" :key="student.id">
            <th>{{ student.name }}</th>
            <th>{{ student.signature }}</th>
            <th>{{ student.note }}</th>
            

          </tr>

        </table>
      </div>
      <DataTable :students="students" />

    </div>
  </div>
</template>

<style lang="scss" scoped>
</style>
