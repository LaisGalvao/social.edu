<template>
  <div class="jumbotron">
    <p class="message" :class="{ 'fade-in': showText }">📚🤝🏽 Em breve: Social.edu!</p>
  </div>
</template>

<style scoped>
.jumbotron {
  padding: 20px;
  border-radius: 10px;
}

.message {
  font-size: 50px;
  color: white;
  text-align: center;
  opacity: 0;
  transition: opacity 2s ease-in-out;
}

.fade-in {
  opacity: 1;
}
</style>

<script setup>
import { ref, onMounted } from 'vue';

const showText = ref(false);

onMounted(() => {
  // Set showText to true after a delay to trigger the fade-in animation
  setTimeout(() => {
    showText.value = true;
  }, 900); // Adjust the delay as needed
});
</script>
