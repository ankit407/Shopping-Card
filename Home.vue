<template>
  <q-layout view="lHh Lpr lFf">
    <div class="q-pa-md">
      <div class="row" style="height: 500px;">
        <div class="col-8 q-pa-md" >
          <h6 class="text-left">Shopping Cart</h6>
        
          <!-- <h6 class="text-right">Shopping Cart</h6> -->
         
          <q-separator   inset />
          <left-component />
          <q-separator   inset />

        </div>
        <div class="col-4">
          <h6>Order Summary</h6>
          <right-component />
          <q-separator inset />
        </div>
      </div>
    </div>
  </q-layout>
</template>
<script>
import leftComponent from "../components/LeftComponent.vue"
import rightComponent from "../components/RightComponent.vue";
import LeftComponent from "../components/LeftComponent.vue";
export default {
  name: "Home-view",
  components: {
    rightComponent,
    leftComponent,
    LeftComponent
},
};
</script>
