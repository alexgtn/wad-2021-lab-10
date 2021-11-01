<template>
<div class="contactus">
  <h2> Contacts </h2>
  <div v-for="contact in contacs" :key="contact.phone"  :email="contact.email">
  <p>  Tel: {{contact.phone}} <br> Email: {{contact.email}} </p>
  </div>  
  </div>
</template>

<script>
export default {
    name: "contactus",
data(){
    return{
contacs:[
        {phone: "+327 999 8888", email: "general@cm.ee"},
        {phone: "+327 999 8889", email: "hr@cm.ee"},
]
}
} 
}
</script>

