<script>
export default {
props:{
  student: String,
}
}
</script>
<template>
 <div class="col-md-8 col-xs-12">
        <h1>Listado</h1>
        <table class="table">
          <tr>
            <th>Nombre</th>
            <th>Materia</th>
            <th>Cualificación</th>
          </tr>
          <tr v-for="(student,key) in students" :key="student.id">
            <th>{{student}}</th>
            <th>{{student.signature}}</th>
            <th>{{student.note}}</th>
          </tr>
          
        </table>
      </div>
</template>


<style lang="scss" scoped>
</style>