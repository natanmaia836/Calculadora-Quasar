<template>
  <q-page class="column flex-center">
    <div class="row">
      <q-input v-model="Display" outlined></q-input>
    </div>
    <div class="row q-mt-sm q-ml-sm">
      <div class="col">
        <q-btn @click="Limpar()" color="green" label="C"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn @click="Dividido()" color="primary" label="/"></q-btn>
      </div>
       <div class="col q-ml-xs">
        <q-btn @click="Porcento()" color="primary" label="%"></q-btn>
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
       <div class="col q-ml-sm q-mt-sm">
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
       <div class="col q-ml-sm q-mt-sm">
        <q-btn @click="Menos()" color="primary" label="_"></q-btn>
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
       <div class="col q-ml-sm q-mt-sm">
        <q-btn color="primary" @click="Virgula()" label="."></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
       <div class="col q-ml-sm">
        <q-btn @click="Clique(0)" label="0"></q-btn>
      </div>
       <div class="col q-ml-md">
        <q-btn size="md" @click="Igual()" color="pink" label="="></q-btn>
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
const teste = ref (0)
const somar = ref (null)
const subtrair = ref (null)
const multiplicar = ref (null)
const dividir = ref (null)
const porcentagem = ref (null)
const fracionado = ref (null)
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
  porcentagem.value = null
  fracionado.value = null
}

const Mais = () => {
  num1.value = Display.value
  console.log(num1.value)
  Display.value = ""
  somar.value = "+"
}

const Menos = () => {
    num1.value = Display.value
  Display.value = ""
  subtrair.value = "-"
  console.log(subtrair.value)
}

const Vezes = () => {
    num1.value = Display.value
  Display.value =""
  multiplicar.value = "*"
  console.log(multiplicar.value)
}

const Dividido = () => {
    num1.value = Display.value
  Display.value = ""
  dividir.value = "/"
  console.log(dividir.value)
}

 const Porcento = () => {
     num1.value = Display.value
   Display.value = ""
   porcentagem.value = "%"
   console.log(porcentagem.value)
 }

 const Virgula = () => {
   Display.value = Display.value + "."
  //  num1.value = Display.value
  //  fracionado.value = "."
  //   console.log(num1.value)
 }

const Igual = () => {

  let v1 = parseFloat(num1.value)
  let v2 = parseFloat(Display.value)

  if (somar.value == "+") {
  Display.value = v1 + v2}

  if (subtrair.value == "-") {
  Display.value = v1 - v2}

    if (multiplicar.value == "*") {
  Display.value = v1 * v2}

    if (dividir.value == "/") {
  Display.value =  v1 / v2}

     if (porcentagem.value == "%") {
  teste.value = v2 / 100
  Display.value = v1 * teste.value}
}



return {
  Igual,
  Vezes,
  Menos,
  Mais,
  Limpar,
  Clique,
  Porcento,
  Dividido,
  Virgula,
  Display,
  num1,
  num2,
  resultado,
  somar,
  subtrair,
  multiplicar,
  dividir,
  porcentagem,
  teste,
  fracionado,
}
},
});

</script>

<style>
</style>
