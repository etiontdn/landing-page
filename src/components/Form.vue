<template>
  <form class="section box" action="">
    <h2 class="title has-text-centered">Contate-nos!</h2>
    <section>
      <b-field label="Nome*" :type="nameInputType" :message="nameInputMessage">
        <b-input
          ref="name"
          icon="account"
          @blur="checkInput('name')"
          @input="checkInput('name')"
          required
          size="is-medium"
          title="Favor preencher"
        ></b-input>
      </b-field>

      <b-field
        label="Email*"
        :type="emailInputType"
        :message="emailInputMessage"
      >
        <b-input
          ref="email"
          type="email"
          icon="email"
          @blur="checkInput('email')"
          @input="checkInput('email')"
          placeholder="exemplo@email.com"
          required
          size="is-medium"
          title="Favor preencher"
          validation-message="Tem certeza que este email esta correto?"
        >
        </b-input>
      </b-field>

      <b-field
        label="Telefone"
        :type="telephoneInputType"
        :message="telephoneInputMessage"
      >
        <b-input
          ref="telephone"
          type="tel"
          icon="phone"
          @blur="checkInput('telephone')"
          @input="checkInput('telephone')"
          placeholder="(32) 99999-9999"
          size="is-medium"
          maxlength="15"
        ></b-input>
      </b-field>

      <b-field
        label="Informações sobre o pedido*"
        :type="infoInputType"
        :message="infoInputMessage"
      >
        <b-input
          required
          ref="info"
          @blur="checkInput('info')"
          @input="checkInput('name')"
          size="is-medium"
          type="textarea"
          title="Favor preencher"
        ></b-input>
      </b-field>
      <p class="help content">
        É necessário preencher todos os campos com *.
      </p>
      <b-field>
        <div class="action-buttons has-text-centered">
          <b-button @click="checkAllInputs()" type="is-primary" size="is-large"
            >Enviar</b-button
          >
          <b-button @click="this.$parent.close" type="is-primary is-inverted" size="is-large"
            >Cancelar</b-button
          >
        </div>
      </b-field>
    </section>
  </form>
</template>
<script>
export default {
  name: 'Form',
  data: function() {
    return {
      inputList: {
        name: {
          id: 'name',
          state: 'Default',
          Wrong: {
            type: 'is-danger',
            message: 'Favor preencher',
          },
          Right: {
            type: 'is-success',
            message: '',
          },
          Default: {
            type: '',
            message: '',
          },
        },
        email: {
          id: 'email',
          state: 'Default',
          Wrong: {
            type: 'is-danger',
            message: 'Tem certeza que este email está correto?',
          },
          Right: {
            type: 'is-success',
            message: '',
          },
          Default: {
            type: '',
            message: '',
          },
        },
        telephone: {
          id: 'tel',
          state: 'Default',
          Wrong: {
            type: '',
            message: '',
          },
          Right: {
            type: 'is-success',
            message: '',
          },
          Default: {
            type: '',
            message: 'Se você preferir se comunicar utilizando o telefone.',
          },
        },
        info: {
          id: 'info',
          state: 'Default',
          Wrong: {
            type: 'is-danger',
            message: 'Favor preencher',
          },
          Right: {
            type: 'is-success',
            message:
              'Informações adicionais sobre o pedido, favor não incluir informações de segurança como endereço, senhas, etc.',
          },
          Default: {
            type: '',
            message:
              'Informações adicionais sobre o pedido, favor não incluir informações de segurança como endereço, senhas, etc.',
          },
        },
      },
    };
  },
  methods: {
    checkInput: async function(input) {
      let inputElement = this.$refs[input];
      console.log(inputElement.checkHtml5Validity());
      if (inputElement.isValid) {
        this.inputList[input].state = 'Right';
      } else {
        this.inputList[input].state = 'Wrong';
      }
    },
    checkAllInputs: function() {
      for (let input of Object.keys(this.inputList)) {
        this.checkInput(input);
      }
    },
  },
  computed: {
    nameInputType: function() {
      return this.inputList.name[this.inputList.name.state].type;
    },
    nameInputMessage: function() {
      return this.inputList.name[this.inputList.name.state].message;
    },
    emailInputType: function() {
      return this.inputList.email[this.inputList.email.state].type;
    },
    emailInputMessage: function() {
      return this.inputList.email[this.inputList.email.state].message;
    },
    telephoneInputType: function() {
      return this.inputList.telephone[this.inputList.telephone.state].type;
    },
    telephoneInputMessage: function() {
      return this.inputList.telephone[this.inputList.telephone.state].message;
    },
    infoInputType: function() {
      return this.inputList.info[this.inputList.info.state].type;
    },
    infoInputMessage: function() {
      return this.inputList.info[this.inputList.info.state].message;
    },
  },
};
</script>
<style lang="scss" scoped>
@import '../main.scss';
form {
  max-width: 550px !important;
  width: 100%;
  margin: auto;
}
div.action-buttons {
  button {
    margin: 5px;
  }
}
</style>
