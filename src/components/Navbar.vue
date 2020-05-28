<template>
  <section class="hero has-background-primary is-small">
    <div class="hero-body">
      <div class="container">
        <div class="logo is-flex">
          <figure class="image is-64x64 is-hidden-mobile">
            <img src="@/assets/potato.svg" alt="placeholder+image" />
          </figure>
          <div class="">
            <h1 class="title">
              Batata Home
            </h1>

            <h2 class="subtitle is-hidden-mobile">
              A solução para todos os seus problemas.
            </h2>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Navbar',
};
</script>
<style lang="scss" scoped>
.logo {
  align-items: stretch;
  .image {
    @media only screen and (min-width: 600px) {
      margin-right: 15px;
    }
  }
}
</style>
