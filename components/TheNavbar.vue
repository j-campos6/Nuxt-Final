<template>
  <!-- Navbar start -->
<div class="row">
  <div class="col-xl-12 col-lg-12 col-sm-12 col-12 bg-dark">
    <b-navbar toggleable type="dark" variant="dark" class="navbar-expand-lg">
      <router-link  class="navbar-brand" to = '/'>TravelJunkie</router-link>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav class="justify-content-center">
      <b-navbar-nav>
          <b-nav-item><NuxtLink to = '/' class="nav-link">Home</NuxtLink></b-nav-item>
          <b-nav-item><NuxtLink to = '/ImagesPage' class="nav-link">Images</NuxtLink></b-nav-item>
          <b-nav-item><NuxtLink to = '/GridPage'  class="nav-link">Bootstrap Grid</NuxtLink></b-nav-item>
          <b-nav-item><NuxtLink to = '/AccordionPage' class="nav-link">Accordion</NuxtLink></b-nav-item>
          <b-nav-item><NuxtLink to = '/ApiPage' class="nav-link">Currencies</NuxtLink></b-nav-item>
      </b-navbar-nav>
    </b-collapse>
    </b-navbar>
  </div>
  <!-- Navbar end -->
</div>
</template>

<script>
export default {
}
</script>

<style lang="css" scoped>
</style>
