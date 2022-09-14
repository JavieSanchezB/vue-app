<script setup>
import { ref } from 'vue';
const counter = ref(0);
const texto = ref(null);

const derechoClick = () =>{
  console.log('Presionaste click Derecho')
  texto.value = "Presionaste click Derecho";
}

const izquierdoClick = () =>{
  console.log('Presionaste click Izquiero')
  texto.value ="Presionaste click Izquiero";
}

const centralClick = () =>{
  console.log('Presionaste click Central')
  texto.value="Presionaste click Central";
}

const incrementar = () =>{
counter.value ++;

}

const decrementar = () =>{
counter.value --;

}
</script> 

<template>
  <h1>Hola vue js</h1>
  
  <div class="btn-group" role="group" aria-label="Basic mixed styles example" >
    
    <button class='btn btn-primary' v-on:click.letf.prevent="izquierdoClick">CLICK IZQUIERDO</button>
    <button class='btn btn-info' v-on:click.middle.prevent="centralClick">CLICK CENRAL</button>
    <button class='btn btn-warning' v-on:click.right.prevent="derechoClick">CLICK DERECHO</button>
   
   
  <button class='btn btn-success' v-on:click="incrementar()">CONTADOR +1</button>
  <button class='btn btn-danger' v-on:click="decrementar()">CONTADOR -1</button>


<div class="alert alert-success" role="alert">
  <h4 class="alert-heading">{{ counter }}</h4>
  <p>Contador</p>
  <hr>
  <p class="mb-0">  {{texto}}</p>
</div>

</div>

</template>

<style>
  h1{
    color:blue
  }
  h2{
    color:chartreuse
  }



</style>