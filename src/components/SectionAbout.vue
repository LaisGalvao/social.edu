<template>
      <div id="about" class="hero is-medium section-about">
      <div class="hero-body">
        <h2>Sobre</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non feugiat
        magna. Sed nec purus vel turpis vehicula sodales.
      </p>
      <p>
        Nulla vitae justo id ligula condimentum eleifend. Ut nec ipsum id lectus
        facilisis ultricies.
      </p>
      <div class="is-flex is-justify-content-center is-flex-wrap-wrap">
        <QuemSomosCard
          v-for="membro in membros"
          :key="membro.nome"
          :nome="membro.nome"
          :foto="membro.foto"
          :descricao="membro.descricao"
          :redesSociais="membro.redesSociais"
        />
      </div>
      </div>
     </div>
</template>
<script>
import QuemSomosCard from './AboutUsCard.vue';

export default {
  components: {
    QuemSomosCard
  },
  data() {
    return {
      membros: [
        {
          nome: 'Fulano de Tal',
          foto: '/fotos/fulano.jpg',
          descricao: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
          redesSociais: {
            facebook: 'https://www.facebook.com/fulano',
            twitter: 'https://www.twitter.com/fulano',
            linkedin: 'https://www.linkedin.com/in/fulano'
          }
        },
        {
          nome: 'Fulano de Tal',
          foto: '/fotos/fulano.jpg',
          descricao: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
          redesSociais: {
            facebook: 'https://www.facebook.com/fulano',
            twitter: 'https://www.twitter.com/fulano',
            linkedin: 'https://www.linkedin.com/in/fulano'
          }
        },
        {
          nome: 'Fulano de Tal',
          foto: '/fotos/fulano.jpg',
          descricao: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
          redesSociais: {
            facebook: 'https://www.facebook.com/fulano',
            twitter: 'https://www.twitter.com/fulano',
            linkedin: 'https://www.linkedin.com/in/fulano'
          }
        }
        // Adicione outros membros da equipe aqui
      ]
    };
  }
};
</script>
  
  <style scoped>
.section-about {
  background-color: #1c4c96;
  color: #ffffff;
 /*  padding: 50px 0; */
}

/* .container {
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
} */

h2 {
  font-size: 24px;
}
</style>
  