<template>
    <div>
        <br><br><br>
       <b-card img-src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQmf-LkcfXUGwwlJuY3i-OJKjGx7pWFC849Ng&usqp=CAU" img-alt="Card image" img-right img-height="500">
      <b-card-text>
        <div>
  <b-form >
      <label for="inline-form-input-name">Id</label>
    <b-form-input
      id="inline-form-input-name"
      class="mb-2 mr-sm-2 mb-sm-0"
      placeholder="Id"
    ></b-form-input>
    <br>
    <label for="inline-form-input-name">Nombre</label>
    <b-form-input
      id="inline-form-input-name"
      class="mb-2 mr-sm-2 mb-sm-0"
      placeholder="Nombre"
    ></b-form-input>
    <br>
    <label for="inline-form-input-name">Dirección</label>
    <b-form-input
      id="inline-form-input-name"
      class="mb-2 mr-sm-2 mb-sm-0"
      placeholder="Dirección"
    ></b-form-input>
    <br>
    <label for="inline-form-input-name">Salario</label>
    <b-form-input
      id="inline-form-input-name"
      class="mb-1 mr-sm-1 mb-sm-0"
      placeholder="Salario"
    ></b-form-input>
    <br>
    <label for="example-datepicker">Fecha de entrada</label>
    <b-form-datepicker id="example-datepicker" v-model="value" class="mb-2"></b-form-datepicker>
    <br>
    <label for="inline-form-input-name">Centro</label>
    <b-form-input
      id="inline-form-input-name"
      class="mb-1 mr-sm-1 mb-sm-0"
      placeholder="Centro"
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
export default {
    name: 'IngresarEmpleado'
}
</script>