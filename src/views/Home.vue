<template>
  <div class="home">
    <!--<Slider :slides="slides" />-->
    <Design/>
  </div>
</template>

<script>
// @ is an alias to /src
//import Slider from "@/components/Slider";
import Design from "@/components/Design";
export default {
  name: "Home",
  components: {
    Design
  },
  mounted() {},
  data() {
    return {
      slides: [
        {
          image:
            "https://images.unsplash.com/photo-1571171637578-41bc2dd41cd2?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80",
          text: "JALEX",
        },
        {
          image:
            "https://images.unsplash.com/photo-1516116216624-53e697fedbea?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80",
          text: "Designing and programming.",
        },
        {
          image:
            "https://images.unsplash.com/photo-1585079542156-2755d9c8a094?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=667&q=80",
          text: "UES",
        },
      ],
    };
  },
  methods: {},
};
</script>

<style>
.home{
  width: 100%;
}
</style>
