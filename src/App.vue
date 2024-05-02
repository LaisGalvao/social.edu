<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TopbarComponent from './components/TopbarComponent.vue';
import SectionAbout from './components/SectionAbout.vue';
import SectionPartners from './components/SectionPartners.vue';
import FooterComponent from './components/FooterComponent.vue';
</script>
<script>
export default {
  data() {
    return {
      showBackToTop: false
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.showBackToTop = window.scrollY > 100;
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

<template>
 <div class="is-flex-direction-row">
  <TopbarComponent />
  <HelloWorld  />
  <SectionAbout />
  <SectionPartners />
  <FooterComponent style="background: #06283f;" />

  <button @click="scrollToTop" class="back-to-top" v-show="showBackToTop">Voltar ao Topo</button>
 </div>
</template>

<style scoped>
.logo {
  height: 6em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.back-to-top {
  position: fixed;
  bottom: 20px;
  right: 20px;
  padding: 10px 20px;
  background-color: #fff;
  color: #06283f;
  border: none;
  border-radius: 5px;
  cursor: pointer;
/*   opacity: 0;
  transition: opacity 0.3s ease; */
}

.back-to-top:hover {
  background-color: #555;
}

.back-to-top.show {
  opacity: 1;
}
</style>
