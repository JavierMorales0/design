<template >
    <div>
    <b-navbar toggleable="sm" type="light" variant="light">
        <b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>

        <b-navbar-brand>Javier Alexander Morales</b-navbar-brand>

        <b-collapse id="nav-text-collapse" is-nav>
        <b-navbar-nav>
            <b-nav-item>
              <router-link to="/" class="link">Home</router-link>
            </b-nav-item>
            <b-nav-item>
              <router-link to="/about" class="link">About</router-link>
            </b-nav-item>
        </b-navbar-nav>
        </b-collapse>
    </b-navbar>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>