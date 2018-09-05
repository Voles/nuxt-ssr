<template>
  <section class="container">
      <div class="links">
        <nuxt-link to="/server-side-rendered/Utrecht" class="button--grey">Server Side Rendered</nuxt-link>
        <nuxt-link to="/client-side-rendered" class="button--grey">Client Side Rendered</nuxt-link>
        <nuxt-link to="/prerendered" class="button--grey">Prerendered</nuxt-link>
      </div>
  </section>
</template>

<script>
export default {
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.links {
  padding-top: 15px;
}
</style>

