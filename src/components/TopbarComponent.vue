<template>
  <b-navbar fixed-top class="is-dark">
      <template #brand>
          <b-navbar-item @click="scrollToTop">
              <img
                  src="https://raw.githubusercontent.com/buefy/buefy/dev/static/img/buefy-logo.png"
                  alt="Lightweight UI components for Vue.js based on Bulma"
              >
          </b-navbar-item>
      </template>
      <template #start>
          <b-navbar-item @click="scrollToSection('#about')">
              Sobre
          </b-navbar-item>
          <b-navbar-item  @click="scrollToSection('#partners')">
              Parceiros
          </b-navbar-item>
          <b-navbar-item @click="scrollToSection('#footer')">
              Contato
          </b-navbar-item>
          <!-- <b-navbar-dropdown label="Info">
              <b-navbar-item href="#">
                  About
              </b-navbar-item>
              
              <b-navbar-item href="#">
                  Contact
              </b-navbar-item>
          </b-navbar-dropdown> -->
      </template>

      <template #end>
          <b-navbar-item tag="div">
              <div class="buttons">
                  <a class="button is-primary">
                      <strong>Sign up</strong>
                  </a>
                  <a class="button is-light">
                      Log in
                  </a>
              </div>
          </b-navbar-item>
      </template>
  </b-navbar>
</template>
<script>
export default {
  methods: {
    scrollToSection(selector) {
      const targetElement = document.querySelector(selector);
      if (targetElement) {
        targetElement.scrollIntoView({
          behavior: 'smooth',
          block: 'start' 
        });
      }
    },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    }
  }
};
</script>

<style scoped>
.is-dark {
  background-color: #06283f !important;
}
</style>