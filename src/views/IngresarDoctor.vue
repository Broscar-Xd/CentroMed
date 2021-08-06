<template>
    <div>
        <br><br><br>
       <b-card img-src="https://static.vecteezy.com/system/resources/previews/001/886/209/non_2x/doctor-medical-cartoon-design-vector.jpg" img-alt="Card image" img-right img-height="500">
      <b-card-text>
        <div>
  <b-form >
    <label for="inline-form-input-id">Id de Empleado</label>
    <select id="center">
      <option v-for="(Employee,index) in listEmployee" :key=index :value="Employee.id">{{Employee.id}}</option>
    </select>
    <br>
    <label for="inline-form-input-fun">Función</label>
    <b-form-input
      id="inline-form-input-name"
      class="mb-1 mr-sm-1 mb-sm-0"
      placeholder="Función"
    ></b-form-input>
    <br>
    <label for="inline-form-input-ex">Experiencia</label>
    <b-form-input
      id="inline-form-input-name"
      class="mb-1 mr-sm-1 mb-sm-0"
      placeholder="Experiencia"
    ></b-form-input>
    <br>

    <b-button variant="primary">Guardar</b-button>
  </b-form>
</div>
      </b-card-text>
    </b-card>
    </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'IngresarDoctor',
  data(){
    return {
      medico:{
        id: "",
        funcion: "",
        experiencia: ""
      },
      listEmployee: ''
    }
  },
  methods:{
    save(){
      this.medico.id = document.getElementById("inline-form-input-id").value;
      this.medico.funcion = document.getElementById("inline-form-input-fun").value;
      this.medico.experiencia = document.getElementById("inline-form-input-ex").value;
      axios.post("http://localhost:3000/api/createMedico",this.medico).then(res=>{
        if(res.status == 200){
          this.medico = res.data;
        }
      }).catch(e=>console.log(e));
      this.medico.id = "";
      this.medico.funcion = "";
      this.medico.experiencia = "";
    },
    list(){
      axios.get("http://localhost:3000/api/listEmployee")
      .then(res=>{
        this.listEmployee=res.data["empleado"];
      })
      .catch(e=>console.log(e));
    },
    save(){
      var selectEmployee = document.getElementById("empleado").value;
      console.log(selectEmployee);
    }
  }
}
</script>