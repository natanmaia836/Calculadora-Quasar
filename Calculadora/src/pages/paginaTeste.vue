<template>
  <q-page class="column flex-center">
    <div class="row">
      <q-input v-model="Display" outlined></q-input>
    </div>
    <div class="row q-ml-sm">
      <div class="col">
        <q-btn @click="Limpar()" color="primary" label="C"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn color="primary" label="/"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn color="primary" label="%"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Mais()" color="primary" label="+"></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
      <div class="col">
        <q-btn @click="Clique(7)" label="7"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Clique(8)" label="8"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Clique(9)" label="9"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Vezes()" color="primary" label="*"></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
      <div class="col">
        <q-btn @click="Clique(4)" label="4"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Clique(5)" label="5"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Clique(6)" label="6"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Menos()" color="primary" label="-"></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
      <div class="col">
        <q-btn @click="Clique(1)" label="1"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Clique(2)" label="2"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Clique(3)" label="3"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn color="primary" @click="Mais()" label="+"></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
      <div class="col">
        <q-btn label="()"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Clique(0)" label="0"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="."></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Igual()" color="primary" label="="></q-btn>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue"
import {ref} from 'vue'
const Display = ref (0)
const num1 = ref (0)
const num2 = ref (0)
const resultado = ref (0)
export default defineComponent({
name: 'paginaTeste',
setup () {

const Clique = (numero) => {
  Display.value = numero
}

const Limpar = () => {
  Display.value = ""
}

const Mais = () => {
  num1.value = Display.value
  Display.value = num1.value + "+"
  console.log(num1.value)
}

const Menos = () => {
    num1.value = Display.value
  Display.value = num1.value + "-"
  console.log(num1.value)
}

const Vezes = () => {
    num1.value = Display.value
  Display.value = num1.value + "*"
  console.log(num1.value)
}

const Igual = () => {
  num2.value = Display.value
  resultado.value = num1.value + num2.value
  Display.value = resultado.value
}

return {
  Igual,
  Vezes,
  Menos,
  Mais,
  Limpar,
  Clique,
  Display,
  num1,
  num2,
  resultado,
}
},
});

</script>

<style>
</style>
