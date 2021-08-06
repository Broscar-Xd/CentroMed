<template>
    <div>
        <br><br><br>
       <b-card img-src="https://st2.depositphotos.com/1663905/10044/v/600/depositphotos_100448476-stock-illustration-medical-health-care-specialties-icons.jpg" img-alt="Card image" img-right img-height="500">
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
      class="mb-1 mr-sm-1 mb-sm-0"
      placeholder="Nombre"
    ></b-form-input>
    <br>
    <label for="inline-form-input-name">Descripción</label>
    <b-form-input
      id="inline-form-input-name"
      class="mb-1 mr-sm-1 mb-sm-0"
      placeholder="Descripción"
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
    name: 'IngresarEspecialidad'
}
</script>