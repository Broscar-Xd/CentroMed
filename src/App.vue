<template>
  <div id="app">
    <b-navbar toggleable="lg" type="dark" variant="info">
      <img src="https://i.pinimg.com/originals/9a/36/b2/9a36b29d0adca32942408b411976ba0b.jpg" class="d-inline-block align-top" alt="Kitten" width="100" height="50">
<b-navbar-brand href="/">Centro Médico Quito</b-navbar-brand> 
      <b-container>
    

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item to="/home" >Ingresar Empleado</b-nav-item>
        <b-nav-item href="/About" >Ingresar Doctor</b-nav-item>
        <b-nav-item :to="{name: 'ingresarDoctor'}" >Reubicar Doctor</b-nav-item>
        <b-nav-item href="#" >Nomina de pagos</b-nav-item>

      </b-navbar-nav>

      <!-- Right aligned nav items -->
      
    </b-collapse>
    </b-container>
  </b-navbar>
  </div>
</template>

