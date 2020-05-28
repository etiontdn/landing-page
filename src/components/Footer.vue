<template>
  <section class="footer has-background-footer has-text-light">
    <div class="container is-fluid-until-desktop">
      <h1 class="title is-2-desktop is-2-mobile">Batata Home</h1> 
      <div class="columns">
        <div class="column">
          <div class="container">
            <div class="about footer-item">
              <h3 class="subtitle is-3 has-text-primary">
                Sobre nós:
              </h3>
              <p class="content is-large">
                Nosso objetivo é trazer o melhor do mundo até a sua casa.
              </p>
              <a class="button is-primary is-outlined is-large" href="#pagecontent">Contate-nos Hoje!</a>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="container">
            <div class="contact footer-item">
              <h3 class="subtitle is-3 has-text-primary">
                Contate-nos:
              </h3>
              <div class="contact-item is-flex">
                <div class="contact-title is-flex">
                  <b-icon
                    icon="whatsapp"
                    size="is-medium"
                    type="is-primary"
                  ></b-icon>
                  <h2 class="subtitle has-text-primary">
                    Whatsapp:
                  </h2>
                </div>
                <h3 class="content is-medium contact-content has-text-light">
                  (32) 99999-9999
                </h3>
              </div>
              <div class="contact-item is-flex">
                <div class="contact-title is-flex">
                  <b-icon
                    icon="phone-outline"
                    size="is-medium"
                    type="is-primary"
                  ></b-icon>
                  <h2 class="subtitle has-text-primary">
                    Telefone:
                  </h2>
                </div>
                <h3 class="content is-medium contact-content has-text-light">
                  (32) 99999-9999
                </h3>
              </div>
              <div class="contact-item is-flex">
                <div class="contact-title is-flex">
                  <b-icon
                    icon="email-outline"
                    size="is-medium"
                    type="is-primary"
                  ></b-icon>
                  <h2 class="subtitle has-text-primary">
                    Email:
                  </h2>
                </div>
                <h3 class="content is-medium contact-content has-text-light">
                  inexistente@batatahome.io
                </h3>
              </div>
              <div class="contact-item is-flex">
                <div class="contact-title is-flex">
                  <b-icon
                    icon="map-marker-outline"
                    size="is-medium"
                    type="is-primary"
                  ></b-icon>
                  <h2 class="subtitle has-text-primary">
                    Local:
                  </h2>
                </div>
                <h3 class="content is-medium contact-content has-text-light">
                  65, Rua inexistente, Lorem Ipsum
                </h3>
              </div>
            </div>
          </div>
        </div>

        <div class="column">
          <div class="container">
            <div class="social footer-item">
            <h3 class="subtitle is-3 has-text-primary">
              Redes sociais:
            </h3>

            <a
              class="content social-link has-text-primary is-flex"
              href="https://www.github.com/etiontdn"
            >
              <b-icon icon="github" size="is-medium" type="is-primary"></b-icon>
              <h3 class="subtitle has-text-primary is-marginless is-5">
                Github
              </h3>

            </a>

            <a class="content social-link has-text-primary is-flex">
              <b-icon
                icon="twitter"
                size="is-medium"
                type="is-primary"
              ></b-icon>
              <h3 class="subtitle has-text-primary is-marginless is-5">
                Twitter
              </h3>
            </a>

            <a href="" class="content social-link has-text-primary is-flex">
              <b-icon
                icon="facebook"
                size="is-medium"
                type="is-primary"
              ></b-icon>
              <h3 class="subtitle has-text-primary is-marginless is-5">
                Facebook
              </h3>
            </a>

            <a href="" class="content social-link has-text-primary is-flex">
              <b-icon
                icon="instagram"
                size="is-medium"
                type="is-primary"
              ></b-icon>
              <h3 class="subtitle has-text-primary is-marginless is-5">
                Instagram
              </h3>
            </a>
          </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!--
  <div><div>Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div></div>
  -->
</template>
<script>
export default {
  name: 'Footer',
};
</script>
<style lang="scss" scoped>
.title,
.content {
  color: inherit !important;
}
.footer-item {
  margin-bottom: 15px;
  &:last-child {
    margin-bottom: 0px;
  }
}
.contact-item {
  margin-bottom: 1.5rem;
  align-items: center;
  justify-content: space-between;
  @media only screen and (max-width: 1440px) {
    flex-direction: column;
    align-items: flex-start;
    .contact-content {
      margin-left: 32px;
      @media only screen and (max-width: 320px) {
        margin-left: 12px;
      }
    }
  }
  &:last-child {
    margin-bottom: 0px;
  }
  .contact-title {
    align-items: center;
  }
  .icon {
    margin-right: 5px;
  }
}

.social-link {
  align-items: center;
  &:hover {
    .subtitle {
      color: white !important;
    }
    .icon {
      color: white !important;
    }
  }
  .subtitle {
    font-weight: 400;
  }
  .icon {
    margin-right: 5px;
  }
}
</style>
