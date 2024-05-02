<!-- QuemSomosCard.vue -->
<template>
  <div class="card">
    <img :src="foto" alt="Foto de {{ nome }}" class="foto">
    <h2>{{ nome }}</h2>
    <p>{{ descricao }}</p>
    <!-- <div class="redes-sociais">
      <a v-for="(link, rede) in redesSociais" :key="rede" :href="link" class="rede-social">
        <img :src="`/icons/${rede}.svg`" alt="Ícone {{ rede }}">
      </a>
    </div> -->
  </div>
</template>

<script>
export default {
  props: {
    nome: String,
    foto: String,
    descricao: String,
    redesSociais: Object // Um objeto onde as chaves são as redes sociais e os valores são os links
  }
};
</script>

<style scoped>
.card {
  width: 300px;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 20px;
  margin: 20px;
}

.foto {
  width: 100%;
  border-radius: 50%;
  margin-bottom: 10px;
}

.redes-sociais {
  display: flex;
}

.rede-social {
  margin-right: 10px;
}

.rede-social img {
  width: 30px;
}
</style>
