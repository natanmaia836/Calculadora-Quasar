<template>
  <q-page class="q-ml-md">

    <div style="margin-left: 200px">
<div class="row q-mt-md">
  <div class="col-3"><q-input  outlined v-model="display" /></div>
  <div class="col-1 q-ml-sm"><q-btn class=" full-width" size="lg"  color="primary" @click="Limpar('')" label="c"></q-btn></div>

</div>
<div class="row q-mt-sm">
  <div class="col-1"><q-btn class="full-width" color="primary" @click="Clique(1)" label="1"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary" @click="Clique(2)" label="2"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary" @click="Clique(3)" label="3"></q-btn></div>
      <div class="col-1 q-ml-sm"><q-btn size="md" color="primary" v-model="barra"  label="/"></q-btn><q-btn class="q-ml-xs" size="md" color="primary" v-model="menos" @click="Subtrair()" label="-"></q-btn></div>

  </div>
  <div class="row q-mt-sm">
  <div class="col-1"><q-btn class="full-width" color="primary" @click="Clique(4)"  label="4"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary" @click="Clique(5)" label="5"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary" @click="Clique(6)"  label="6"></q-btn></div>
      <div class="col-1 q-ml-sm"><q-btn size="md" color="primary" v-model="vezes"  label="*"></q-btn><q-btn class="q-ml-xs" size="md" color="primary" v-model="ponto"  label="."></q-btn></div></div>

  <div class="row q-mt-sm">
  <div class="col-1"><q-btn class="full-width" color="primary" @click="Clique(7)" label="7"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary" @click="Clique(8)" label="8"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary" @click="Clique(9)" label="9"></q-btn></div>
  </div>
  <div class="row q-mt-sm">
    <div class="col-1"><q-btn class="full-width" color="primary" @click="Soma()" label="+"></q-btn></div>
    <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary" @click="Clique(0)" label="0"></q-btn></div>
    <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary" @click="Resultado()" label="="></q-btn></div>
  </div>
  </div>
  </q-page>
</template>

<script>
import {ref} from 'vue'
export default {
  name: 'IndexPage',


setup () {
const display = ref()
const primeironumero = ref (0)
const segundonumero = ref (0)
const resultado = ref (0)


const Clique = (numero) => {
   display.value = numero
   //console.log (numero)

}

const Subtrair = () => {
  primeironumero.value = display.value
  display.value = primeironumero.value
  console.log (primeironumero.value)
}


const Limpar = () => {
 display.value = ""
   }

const Soma = () => {
  primeironumero.value = display.value
  display.value = primeironumero.value
  console.log (primeironumero.value)
}

const Resultado = () => {
   segundonumero.value = display.value
   resultado.value = primeironumero.value + segundonumero.value
    display.value = resultado.value
  console.log(resultado.value)
     segundonumero.value = display.value
   resultado.value = primeironumero.value - segundonumero.value
    display.value = resultado.value
}



 return {
   Resultado,
   Soma,
  Limpar,
  Clique,
  Subtrair,
  primeironumero,
  segundonumero,
  resultado,

  display,
  mais: '+',
  menos: '-',
  vezes: '*',
  barra: '/',
  ponto: '.',
  igual: '=',
};
},
};

</script>
