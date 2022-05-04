<template>
  <q-page class="q-ml-md">
    <div style="margin-left: 200px">
<div class="row q-mt-md">
  <div class="col-3"><q-input outlined v-model="text" /></div>
  <div class="col-1 q-ml-sm"><q-btn class=" full-width" size="lg"  color="primary" label="C"></q-btn></div>

</div>
<div class="row q-mt-sm">
  <div class="col-1"><q-btn class="full-width" color="primary"  label="1"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary"  label="2"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary"  label="3"></q-btn></div>
      <div class="col-1 q-ml-sm"><q-btn size="md" color="primary"  label="/"></q-btn><q-btn class="q-ml-xs" size="md" color="primary"  label="-"></q-btn></div>

  </div>
  <div class="row q-mt-sm">
  <div class="col-1"><q-btn class="full-width" color="primary"  label="4"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary"  label="5"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary"  label="6"></q-btn></div>
      <div class="col-1 q-ml-sm"><q-btn size="md" color="primary"  label="*"></q-btn><q-btn class="q-ml-xs" size="md" color="primary"  label="."></q-btn></div></div>

  <div class="row q-mt-sm">
  <div class="col-1"><q-btn class="full-width" color="primary"  label="7"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary"  label="8"></q-btn></div>
  <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary"  label="9"></q-btn></div>
  </div>
  <div class="row q-mt-sm">
    <div class="col-1"><q-btn class="full-width" color="primary"  label="+"></q-btn></div>
    <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary"  label="0"></q-btn></div>
    <div class="col-1 q-ml-sm"><q-btn class="full-width" color="primary"  label="="></q-btn></div>
  </div>
  </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>
