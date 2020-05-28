<template>
  <div class="section">
    <div class="container">
      <div class="columns is-flex-desktop center-text">
        <div class="column">
          <div class="content has-text-centered-touch">
            <h2 class="title is-2">Batata Home</h2>
            <p class="content is-medium">
              Batatas até você sem que você precise sair de casa!
            </p>
            <p class="content is-medium">
              O melhor legume do mundo entregue até a porta de sua casa 4 vezes por mês!
            </p>
          </div>
        </div>
        <div class="column">
          <figure class="image">
            <img
              src="@/assets/potato.svg"
              alt="placeholder+image"
            />
          </figure>
        </div>
      </div>
      <div class="content has-text-centered">
        <b-button @click="showParentForm" type="is-primary" size="is-large"
          >Contatar Agora</b-button
        >
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Content',
  methods: {
    showParentForm: function () {
      this.$parent.showForm = true;
    }
  }
};
</script>
<style lang="scss" scoped>

.image {
  @media only screen and (max-width: 799px) {
    width: 50%;
    margin: auto;
  }
}

.center-text {
  align-items: center;
}

</style>
