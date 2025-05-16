<template>
  <div>
    <h1>Informe a URL da imagem:</h1>
    <input
      type="url"
      :style="input"
      v-model="inputValue"
      placeholder="https://example.com/image.jpg"
    />
    <p>{{ inputValue }}</p>
  </div>
</template>

<style scoped>
div {
  background-color: rgb(87, 83, 77);
  padding: 20px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: 'JetBrains Mono';
  font-size: clamp(1rem, 1vw, 1rem);
}
input {
  width: clamp(20rem, 10vw, 25rem);
  margin-top: 10px;
  padding: 5px;
  border: none;
  border-radius: 3px;
  font-family: 'JetBrains Mono';
  font-size: 1rem;
}
</style>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
const inputValue = ref(null)
const inputSize = ref(null)
const input = ref(null)
onMounted(() => {
  if (inputValue.value !== null || inputValue.value !== '') {
    if (inputValue.value.length > 32) {
      input:  = +1
    }
  }
})
</script>
