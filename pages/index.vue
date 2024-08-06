<template>
  <div>
    <div class="intro">
      <h1>Cascading Style Sheets</h1>
      <h2>By Ricsi</h2>
      <button
        type="button"
        class="btn btn-dark"
        @click="fetchCatImage"
        style="margin: 20px"
      >
        More cats
      </button>
      <img
        v-if="catImage"
        :src="catImage.url"
        :alt="'Cat image ' + catImage.id"
      />
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const catImage = ref(null);

const fetchCatImage = async () => {
  const response = await fetch("https://api.thecatapi.com/v1/images/search");
  const data = await response.json();
  catImage.value = data[0];
};

onMounted(fetchCatImage);
</script>

<style>
.intro {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}
</style>
