<template>
  <div id= "comp-list-one"> 
  <h1> Book list one  </h1>
  <!-- <h1> {{testpro}}</h1> -->
  
   <!-- <li  class="item" v-for = "product in productList" :key="product.id"> -->
   
   <ul>
   <li  class="item" v-for = "product in productListsale" :key="product.id">
   <span class="author"> <b> Author: </b>  {{product.author}} </span> <br> 
   <span class="book"> <b>Book:</b>  {{product.book}} </span> <br> 
   <span class="goodreads"> <b>Goodreads:</b>  {{product.goodreads}} </span> <br> 
   <span class="price"> Price:{{product.price}} </span> 
   </li>
  </ul>

<!--   <div v-for="product in productList" :key="product.id">
  <p>  Author: {{product.author}} <br> Book: {{product.book}}  Price: {{product.price}} </p> </div> -->

<!--   <p class="item" v-for="product in productList" :key="product.id">
  <span class="author"> <b>Author:</b> {{product.author}} </span>  <br> 
  <span class="book"> <b>Book:</b>  {{product.book}} </span>  <br> 
  <span class="goodreads"> <b>Goodreads:</b>  {{product.goodreads}} </span>  <br> 
  <span class="price"> Price: € {{product.price}} </span>  </p>  -->

 </div>
 </template>

  <!-- props: ["productList"], -->

 


<script>
export default {
name: "product_compo_1",
data: function() {
return {
}},

computed: {

productList(){ return this.$store.state.productList  },

productListsale(){ return this.$store.getters.productListsale  },


testpro(){ return this.$store.state.testString  },
 
 }


}
</script>

<style scoped>
    .item{
    background: rgb(47, 255, 141);
    margin-bottom: 5px;
    padding: 3px 5px;
}
#comp-list-one{
    background: #ffb1b1;
    box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
    margin-bottom: 30px;
    padding: 10px 20px;
}
#comp-list-one ul{
    padding: 0;
}
#comp-list-one li{
    display: inline-block;
    margin-right: 10px;
    margin-top: 10px;
    padding: 20px;
    background: rgba(255,255,255,0.7);
}
.price{
    font-weight: bold;
    color: #E8800C;
}
</style>