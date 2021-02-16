<template>
  <div class="home" style="width:100%">
    <AppSlider :slides="slides" />
    <div class="element">
      <p class="text-muted display-4">
        Hello
      </p>
      <div class="container">
        <div class="row">
          <div class="col">
            <div class="ul">
              <li>Elemento de la lista</li>
            </div>
          </div>
          <div class="col">
            <div class="ul">
              <li>Elemento de la lista</li>
            </div>
          </div>
          <div class="col">
            <div class="ul">
              <li>Elemento de la lista</li>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import AppSlider from "@/components/AppSlider";
export default {
  name: "Home",
  components: {
    AppSlider,
  },
  mounted() {},
  data() {
    return {
      slides: [
        {
          image:
            "https://images.unsplash.com/photo-1483000805330-4eaf0a0d82da?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=334&q=80",
          text: "Consola",
        },
        {
          image:
            "https://images.unsplash.com/photo-1510915361894-db8b60106cb1?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80",
          text: "Guitarra acústica",
        },
        {
          image:
            "https://images.unsplash.com/photo-1462965326201-d02e4f455804?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=750&q=80",
          text: "Guitarra Electrica",
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
