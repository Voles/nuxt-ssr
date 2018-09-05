<template>
  <div>
    <ul>
      <li>
        Server Side Rendering (SSR) makes the initial request fast as it is being rendered on the server.
        Prerendering allows creating static files of your routes. These can be served for the initial requests
      </li>
      <li>
        For both strategies, after the initial request the app is hydrated (the page becomes an actual SPA / interactive) and subsequent navigation is done through an SPA.
      </li>
      <li>
        The advantage of SSR is that unforeseen dynamic URLs can also be rendered server-side.
        For prerendering, you have to know upfront which pages you want to render.
      </li>
      <li>
        It makes sense to prerender all pages. The sections which would need dynamic data (eg. user-data, browser-data like geolocation) could be added as a component.
        Because the data from `asyncData` is processed for SSR/prerender, but components are not.
      </li>
    </ul>
    <section class="container">
      <div class="links">
        <nuxt-link to="/cities/Maastricht" class="button--grey">Prerendered</nuxt-link>
        <nuxt-link to="/cities/Amsterdam" class="button--grey">Not prerendered</nuxt-link>
        <nuxt-link to="/client-side-rendered" class="button--grey">CSR (because async data loaded in component)</nuxt-link>
      </div>
    </section>
  </div>
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

