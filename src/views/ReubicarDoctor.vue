<template>
    <div>
        <br><br><br>
       <b-card img-src="https://prints.ultracoloringpages.com/f5da751484fa8313f44617f030727404.png" img-alt="Card image" img-right img-height="500">
      <b-card-text>
        <div>
  <b-form >
    <label for="inline-form-input-name">Seleccione el Doctor</label>
    <div>
        <b-dropdown id="dDoctor" text="Seleccione el doctor" class="m-md-2">
          <option v-for="(Medico,index) in listMedico" :key=index :value="Medico.id">{{Medico.id}}</option>
        </b-dropdown>
    </div>

    <br>
    <label for="inline-form-input-name">Seleccione el Centro al que se rerá reubicado</label>
    <div>
        <b-dropdown id="dDoctor" text="Seleccione el centro" class="m-md-2">
        </b-dropdown>
    </div>
    <br>
    <b-button variant="primary" id="btnGuardarReubica">Guardar</b-button>
  </b-form>
</div>
      </b-card-text>
    </b-card>
    </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'ReubicarDoctor',
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