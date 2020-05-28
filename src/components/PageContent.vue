<template>
  <div class="wrapper is-flex">
    <div class="section is-flex">
      <Content></Content>
      <b-modal
        :active.sync="showForm"
        trap-focus
        :destroy-on-hide="false"
        aria-role="dialog"
        aria-modal
      >
        <Form></Form>
      </b-modal>
    </div>
  </div>
</template>

<script>
import Content from './Content.vue';
import Form from './Form.vue';

export default {
  name: 'PageContent',
  components: {
    Content,
    Form,
  },
  data: function () {
    return {
      showForm: false,
    }
  }
};
</script>

<style lang="scss">
.wrapper {
  min-height: 100vh;
  .section {
    max-width: 960px;
    align-items: center;
    flex-direction: column;
  }
  justify-content: center;
  align-items: center;
}
</style>
