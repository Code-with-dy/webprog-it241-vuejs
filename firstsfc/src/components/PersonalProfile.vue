<script setup>
import { ref } from 'vue';

const message = ref('Personal Portfolio');
const name = ref('Dylan D. Villanueva');

// Updated with valid placeholder images
const products = ref([
  { id: 1, title: 'Daily Workout', desc: 'Build strength and discipline', price: 'Free', btn: 'Start Now', img: 'https://images.unsplash.com' },
  { id: 2, title: 'Focused Learning', desc: 'Learn something new every day', price: 'Free', btn: 'Start Learning', img: 'https://images.unsplash.com' },
  { id: 3, title: 'Strong Mindset', desc: 'Discipline beats motivation', price: 'Free', btn: 'Build Mindset', img: 'https://images.unsplash.com' },
  { id: 4, title: 'Mindful Meditation', desc: 'Clear your mind and find peace', price: 'Free', btn: 'Start Meditating', img: 'https://images.unsplash.com' },
  { id: 5, title: 'Productivity Hacks', desc: 'Maximize your day effectively', price: 'Free', btn: 'Learn More', img: 'https://images.unsplash.com' }
]);
</script>

<template>
  <div class="app-wrapper">
    <header class="main-header">
      <h1>{{ message }}</h1>
    </header>

    <section class="container profile-grid">
      <!-- Profile Box -->
      <div class="info-box about">
        <h2>About Me</h2>
        <p>I am <strong>{{ name }}</strong>, 19 years old.</p>
      </div>

      <!-- House Box (Fixed unclosed section) -->
      <div class="info-box house">
        <h2>Personal Gallery</h2>
        <div class="product-list">
          <div v-for="product in products" :key="product.id" class="card">
            <img :src="product.img" :alt="product.title" class="card-img">
            <h3>{{ product.title }}</h3>
            <p>{{ product.desc }}</p>
            <button>{{ product.btn }}</button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
/* Basic layout to make the fix look good */
.product-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-top: 20px;
}
.card {
  border: 1px solid #ddd;
  padding: 15px;
  border-radius: 8px;
  text-align: center;
}
.card-img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 4px;
}
</style>
