<template>
<div class="products">
  <h2> Our Products page</h2>


      <product_compo_1 :productList="productList"></product_compo_1>

      <button v-on:click="IncreasePrice ">  Increase price </button>
      <button v-on:click="DecreasePrice"> Decrease price </button>

      <product_compo_2 :productList="productList" ></product_compo_2>

 
</div>

<!--       <product_compo_1 ></product_compo_1>
      <product_compo_2 ></product_compo_2> -->


      <!-- <product_compo_2 :postsUrl="postsUrl" ></product_compo_2> -->


<!--        <div v-for="product in productList" :key="product.author"  :book="product.book">
             <p>  Author: {{product.author}} <br> Book: {{product.book}} </p> 
       </div>

<ul>
   <li v-for = "product in productList" :key="product.id">
   <span class="author"> Author: {{product.author}} </span> 
   <span class="book"> Book: {{product.book}} </span> 
   <span class="price"> Price: {{product.price}} </span> 
   </li>
  </ul>

</div> -->
</template>

<script>

import product_compo_1 from "@/components/product_compo_1.vue"; 
import product_compo_2 from "@/components/product_compo_2.vue";
 

export default {
  name: "Products",
   components: {
      product_compo_1,   product_compo_2
  },
//props: ["productList",  "postsUrl" ],
  data(){
    return{
productList:[
        {id: 1, author: "Charlotte Bronte", book: "Jane Eyre", goodreads: "4.1/5", price: 20},
        {id: 2, author: "Margaret Mitchell", book: "Gone with the Wind", goodreads: "4.3/5", price: 22},
        {id: 3, author: "Anthony Burgess", book: "A Clockwork Orange", goodreads: "4/5",  price: 13},
        {id: 4, author: "Fyodor Dostoevsky" , book: "Crime and Punishment", goodreads: "4.2/5",  price: 18}
],
postsUrl: null, 
}
},
 
/* created() {
fetch('https://jsonplaceholder.typicode.com/posts')
.then(res => res.json())
.then(data => this.postsUrl = data)
.then(console.log(this.postsUrl))
} */



methods: {

IncreasePrice: function() {
  this.$store.commit("IncreasePrice")
  /*   this.$store.state.productList.forEach(product => {
      product.price -= 1;
    }); */
   },

/* IncreasePrice: function() {
  this.$store.dispatch("IncreasePriceAct")
  
   },

DecreasePrice: function() {
  this.$store.dispatch("DecreasePrice")
  
   }, */

DecreasePrice() {
  this.$store.commit("DecreasePrice")
  /*   this.$store.state.productList.forEach(product => {
      product.price += 1;
    }); */
   }
}
}
</script>