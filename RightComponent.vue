<template>
  <div  class="q-pa-md">
    
  <h6>ITEMS 3</h6>
    <div  class="text-right">
      <b>$457.98</b>
    </div>
  </div>
  <div>
    <h6>SHIPPING</h6>
    <div>
      <q-select v-model="model" :options="options" label="Standard Delivery" />
    </div>
  </div>
  <div>
    <h6>PROMO CODE</h6>
    <div>
      <q-input v-model="text" label="Enter Your Code" />
    </div><br><br>
    <q-btn
      color="red"
      label="Apply"
    />
   <q-separator inset />
 <div>
<!-- <q-badge>justify-center</q-badge> -->
    <h6>TOTAL COSTS</h6>
    <div class="text-right">
      <b>$457.98</b>
    </div>
<q-btn color="primary" class="full-width" label="CHECKOUT" />
  </div>

  </div>
</template>

<script>
export default {
  name: "right-component",

   data () {
      return {
        // model: ref(),
        options: ['Google','Facebook','Instagram','Wathsapp']
      }
    }
};
</script>

<style>
</style>