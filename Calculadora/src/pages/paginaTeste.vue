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
        <q-btn @click="Dividido()" color="primary" label="/"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn  color="primary" label="%"></q-btn>
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
const Display = ref ("")
const num1 = ref ("")
const num2 = ref ("")
const resultado = ref (0)
const somar = ref (null)
const subtrair = ref (null)
const multiplicar = ref (null)
const dividir = ref (null)
//const porcentagem = ref (null)
export default defineComponent({
name: 'paginaTeste',
setup () {

const Clique = (numero) => {
  Display.value = Display.value + numero
}

const Limpar = () => {
  Display.value = ""
  somar.value = null
  subtrair.value = null
  multiplicar.value = null
  dividir.value = null
  //porcentagem.value = null
}

const Mais = () => {
  num1.value = Display.value
  Display.value = ""
  somar.value = "+"
  console.log(somar.value)
}

const Menos = () => {
    num1.value = Display.value
  Display.value = num1.value + "-"
  subtrair.value = "-"
  console.log(subtrair.value)
}

const Vezes = () => {
    num1.value = Display.value
  Display.value = num1.value + "*"
  multiplicar.value = "*"
  console.log(multiplicar.value)
}

const Dividido = () => {
    num1.value = Display.value
  Display.value = num1.value + "/"
  dividir.value = "/"
  console.log(dividir.value)
}

// const Porcento = () => {
//     num1.value = Display.value
//   Display.value = num1.value + "%"
//   porcentagem.value = "%"
//   console.log(porcentagem.value)
// }

const Igual = () => {
  let v1 = parseInt(Display.value)
  let v2 = parseInt(num1.value)
  Display.value = v1 + v2
  //num2.value = Display.value
  //resultado.value = num1.value + num2.value
  //Display.value = resultado.value
// if (somar.value == "+") {
//   num2.value = Display.value
//   resultado.value = num1.value + num2.value
//   Display.value = resultado.value
// }
// if (subtrair.value == "-") {
//   num2.value = Display.value
//   resultado.value = num2.value - num1.value
//   Display.value = resultado.value
// }
// if (multiplicar.value == "*") {
//   num2.value = Display.value
//   resultado.value = num1.value * num2.value
//   Display.value = resultado.value
// }
// if (dividir.value == "/") {
//   num2.value = Display.value
//   resultado.value = num1.value / num2.value
//   Display.value = resultado.value
// }
// if (porcentagem.value == "%") {
//   num2.value = Display.value
//   resultado.value = (num2.value) / 100
//   Display.value = resultado.value
// }

console.log (resultado.value)
}

return {
  Igual,
  Vezes,
  Menos,
  Mais,
  Limpar,
  Clique,
  //Porcento,
  Dividido,
  Display,
  num1,
  num2,
  resultado,
  somar,
  subtrair,
  multiplicar,
  dividir,
  // porcentagem,
}
},
});

</script>

<style>
</style>
