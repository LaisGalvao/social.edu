<template>
  <section id="partners" class="hero is-medium section-partners">
    <div class="container">
      <h2>Quer se tornar parceiro?</h2>
      <!-- <div class="partners-list">
          <img src="" alt="Parceiro 1">
          <img src="" alt="Parceiro 2">
        </div> -->
      <!-- Botão "Quer se tornar parceiro?" -->
      <button @click="openModal" class="button is-primary">
        Clique aqui
      </button>

      <!-- Modal -->
      <b-modal v-model="modalActive" title="Torne-se nosso parceiro">
        <form @submit.prevent="sendEmail">
          <b-field label="Seu Nome">
            <b-input
              v-model="nome"
              required
              placeholder="Digite seu nome"
            ></b-input>
          </b-field>
          <b-field label="Seu Email">
            <b-input
              v-model="email"
              type="email"
              required
              placeholder="Digite seu email"
            ></b-input>
          </b-field>
          <b-field label="Mensagem">
            <b-input
              v-model="mensagem"
              type="textarea"
              placeholder="Digite sua mensagem"
            ></b-input>
          </b-field>
          <div class="buttons">
            <b-button type="submit" native-type="submit" class="is-primary"
              >Enviar</b-button
            >
            <b-button @click="closeModal">Cancelar</b-button>
          </div>
        </form>
      </b-modal>
    </div>
  </section>
</template>
  
<script>
export default {
  data() {
    return {
      modalActive: false,
      nome: "",
      email: "",
      mensagem: "",
    };
  },
  methods: {
    openModal() {
      this.modalActive = true;
    },
    closeModal() {
      this.modalActive = false;
      // Limpar os campos do formulário ao fechar o modal
      this.nome = "";
      this.email = "";
      this.mensagem = "";
    },
    sendEmail() {
      // Aqui você pode implementar o envio do email para o destinatário desejado
      console.log("Enviando email...");
      console.log("Nome:", this.nome);
      console.log("Email:", this.email);
      console.log("Mensagem:", this.mensagem);
      // Após o envio, feche o modal
      this.closeModal();
    },
  },
};
</script>

  <style scoped>
.section-partners {
  background-color: #607ec9;
  color: #ffffff;
  padding: 50px 0;
}
/*   
  .container {
    max-width: 1200px;
    margin: 0 auto;
    text-align: center;
  }
   */
h2 {
  font-size: 24px;
}

.partners-list {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

.partners-list img {
  max-width: 150px;
  margin: 0 20px;
}
</style>
  