<template>
  <q-page class="column flex-center">
    <div class="row">
      <q-input outlined></q-input>
    </div>
    <div class="row q-ml-sm">
      <div class="col">
        <q-btn label="C"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="/"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="%"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="+"></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
      <div class="col">
        <q-btn label="7"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="8"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="9"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="*"></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
      <div class="col">
        <q-btn label="4"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="5"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="6"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="-"></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
      <div class="col">
        <q-btn label="1"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="2"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="3"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="+"></q-btn>
      </div>
    </div>
        <div class="row q-ml-sm">
      <div class="col">
        <q-btn label="0"></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="() "></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="."></q-btn>
      </div>
       <div class="col q-ml-sm">
        <q-btn label="="></q-btn>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "@vue/runtime-core"

export default defineComponent({
name: 'paginaTeste',
setup () {

console.log("Treinamento")
},
});
</script>

<style>
</style>
