<template>
  <div id="app">
    
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link :to="{ name: 'products' }"> Products </router-link> |
      <router-link to="/about">About</router-link> |
      <!-- <router-link to="/contactus">Contacts</router-link> -->
      <router-link :to="{ name: 'contactus' }"> Contacts </router-link>
      <router-view />

    <!--   <products :productList="productList"></products> -->

      <!-- <product_compo_1 :productList="products"></product_compo_1>
      <product_compo_2 :productList="products"></product_compo_2> -->
    </div>
   
  </div>
</template>


<script>
//import Products from './views/Products.vue'
/* import product_compo_1 from "@/components/product_compo_1.vue";
import product_compo_2 from "@/components/product_compo_2.vue"; */
//import FirstComponent from './components/first-component.vue';


export default {
    name: 'App',
    components: {
        //Products
  //  product_compo_1, product_compo_2, FirstComponent
  /*   product_compo_1, product_compo_2 */
  },
  //props: ["productList", /* "postsUrl" */],
data(){
    return{

      productList:[
        {id: 1, author: "Charlotte Bronte", book: "Jane Eyre", goodreads: "4.1/5", price: 20},
        {id: 2, author: "Margaret Mitchell", book: "Gone with the Wind", goodreads: "4.3/5", price: 22},
        {id: 3, author: "Anthony Burgess", book: "A Clockwork Orange", goodreads: "4/5",  price: 13},
        {id: 4, author: "Fyodor Dostoevsky" , book: "Crime and Punishment", goodreads: "4.2/5",  price: 18}
],
}
} 
}
</script>


<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
