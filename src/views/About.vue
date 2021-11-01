<template>
  <div class="about">
    <h1>This is an about page</h1>
    <firstcomponent firstmsg  ="Hi there,  first message from About.vue"/>
  </div>
</template>

<script>
// @ is an alias to /src
import firstcomponent from "@/components/first-component.vue";

export default {
  name: "About",
  components: {
    firstcomponent,
  }
  };
</script>
