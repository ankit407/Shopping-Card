<template>
  <div class="q-pa-md">
    <div class="row">
      <div class="col">PRODUCT DETAILS</div>
      <div class="col">QUANTITY</div>
      <div class="col">PRICE</div>
      <div class="col">TOTAL</div>
    </div>
    <div class="row" v-for="item in product" :key="item">
      <div class="col">{{ item.name }}</div>
      <div class="col">
       <input type="number" min="1" v-model="item.quantity"/>
      <!-- <div class="col">{{ item.quantity }}</div> -->

      
      </div>
      <div class="col">
        {{ item.price }}
      </div>
      <div class="col">
        {{ Math.ceil(item.quantity * item.price) }}
      </div>
    <!-- <q-separator color="blue"  inset /> -->
    </div>
  </div>
<div class="text-center">
<h5> Total:  {{total}}</h5>
</div>
</template>

<script>
export default {
  name: "left-component",
  data() {
    return {
      product: [
        {
          name: "Shirt",
          quantity: "6",
          price: 500,
         
        },
         {
          name: "T-Shirt",
          quantity: "4",
          price: 300,
         
        },
  {
          name: "Formal-Dress",
          quantity: "9",
          price: 200,
         
        },
  {
          name: "Jeans",
          quantity: "10",
          price: 100,
         
        },
      ],
  total: 0,
    };
  },
created(){
this.calculateAmount();
console.log(this.price)
},
methods:{
calculateAmount(){
this.total = 0;
this.product.forEach((item)=>{
this.total = this.total + Math.ceil(item.quantity * item.price)
});
},
},
watch: {
product:{
handler () {
this.calculateAmount();
},
deep:true,
}
}
};
</script>
