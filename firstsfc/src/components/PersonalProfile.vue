<script setup>
import { ref } from 'vue';

const message = ref('Personal Portfolio');
const name = ref('Dylan D. Villanueva');

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
    <header>
      <h1>{{ message }}</h1>
      <p>Created by {{ name }}</p>
    </header>

    <main>
      <!-- About Section -->
      <section class="container">
        <div class="about-box">
          <h2>About Me</h2>
          <p>I am <strong>{{ name }}</strong>, 19 years old. Focused on building discipline and technical skills.</p>
        </div>
      </section>

      <!-- Products Grid -->
      <section class="products">
        <div v-for="item in products" :key="item.id" class="card">
          <div class="image" :style="{ backgroundImage: `url(${item.img})` }"></div>
          <h3>{{ item.title }}</h3>
          <p class="desc">{{ item.desc }}</p>
          <p class="price">{{ item.price }}</p>
          <button>{{ item.btn }}</button>
        </div>
      </section>
    </main>

    <footer>
      <p>&copy; 2024 {{ name }}. All rights reserved.</p>
    </footer>
  </div>
</template>

<style>
/* Your requested design styles applied below */
body {
  margin: 0;
  font-family: 'Arial', sans-serif;
  background: #121212; 
  color: #f1f1f1; 
  text-align: center;
  line-height: 1.6;
}

h1 {
  background: #1f1f1f;
  font-size: 2.8rem;
  color: #f1f1f1; 
  text-shadow: 2px 2px 5px rgba(255, 255, 255, 0.2); 
  margin: 0;
  padding-top: 20px;
}

h2 {
  font-size: 2rem;
  color: #e74c3c; 
}

p {
  font-size: 1.1rem;
  color: #bdc3c7; 
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.2); 
}

.container {
  display: flex;
  justify-content: center;
  margin-top: 30px;
  padding: 20px;
}

/* Aligned the "About" box to be centered and readable */
.about-box {
  background-color: #1f1f1f; 
  color: #fff;
  max-width: 600px;
  width: 100%;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.4); 
  text-align: center; 
}

header {
  background: #1f1f1f;
  color: #fff;
  padding: 20px 0;
}

header p {
  color: #f39c12; 
  margin-top: 10px;
}

.products {
  display: flex;
  justify-content: center;
  gap: 25px;
  padding: 40px 20px;
  flex-wrap: wrap;
}

.card {
  background: #1f1f1f; 
  width: 300px;
  text-align: center;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease;
  padding-bottom: 20px;
  overflow: hidden;
}

.card:hover {
  transform: translateY(-15px);
}

.image {
  height: 180px;
  background-size: cover;
  background-position: center;
  margin: 10px;
  border-radius: 8px;
}

h3 {
  font-size: 1.5rem;
  color: #e74c3c; 
  margin-top: 15px;
}

.desc {
  font-size: 0.95rem;
  color: #bdc3c7; 
  margin-bottom: 15px;
  padding: 0 15px;
}

.price {
  color: #2ecc71; 
  font-weight: bold;
  margin-bottom: 15px;
}

button {
  padding: 10px 25px;
  background: #e74c3c; 
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-weight: bold;
  transition: background 0.3s ease;
}

button:hover {
  background: #c0392b; 
}

footer {
  background-color: #1f1f1f;
  color: white;
  padding: 30px;
  margin-top: 40px;
}
</style>
