<template>
    <div>
        <br><br><br>
       <b-card img-src="https://www.popularenlinea.com/SiteCollectionImages/personas/joven/Articulos/Diciembre/Imagen-Blog.png" img-alt="Card image" img-right img-height="500">
      <b-card-text>
          
        <div>
  <b-form >
    <label for="inline-form-input-name">Seleccione el doctor</label>
    <div>
        <b-dropdown id="dDoctor" text="Seleccione el doctor" class="m-md-2">
          <option v-for="(Medico,index) in listMedico" :key=index :value="Medico.id">{{Medico.id}}</option>
        </b-dropdown>
    </div>
    <br>
    <b-button variant="primary" id="btnGenerarNomina">Generar nómina</b-button>
    <br>
    <div id="nomina">
        
    </div>
    <br>
    <b-button variant="primary" id="btnGuardarPDF">Guardar como PDF</b-button>
  </b-form>
</div>
      </b-card-text>
    </b-card>
    </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'nominaPagos',
  data(){
    return {
      listMedico: ''
    }
  },
  methods:{
    
    list(){
      axios.get("http://localhost:3000/api/listMedico")
      .then(res=>{
        this.listMedico=res.data["medico"];
      })
      .catch(e=>console.log(e));
    },
    save(){
      var selectMedico = document.getElementById("medico").value;
      console.log(selectMedico);
    }
  }
}
</script>