<template>
  <div class= "first-comp"> 
  <h1> This is our first componenet </h1>
  <h2>{{ msgFromFirstCom }}</h2>
  <h3>{{ firstmsg }}</h3>
 </div>
 </template>

<script>
export default {
  props: ["firstmsg"],
data: function() {
return {
  msgFromFirstCom: "Hi there,  first message from firstcomponent.vue"
  }; }
}
</script>

<style scoped>
h1 {
font-size: 10px;
}
</style>