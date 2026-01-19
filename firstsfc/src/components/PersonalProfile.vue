<script setup>
import { ref } from 'vue';

const message = ref('Personal Portfolio');
const name = ref('Dylan D. Villanueva');

const products = ref([
  { id: 1, title: 'Daily Workout', desc: 'Build strength and discipline', price: 'Free', btn: 'Start Now', img: 'https://images.unsplash.com' },
  { id: 2, title: 'Focused Learning', desc: 'Learn something new every day', price: 'Free', btn: 'Start Learning', img: 'https://images.unsplash.com' },
  { id: 3, title: 'Strong Mindset', desc: 'Discipline beats motivation', price: 'Free', btn: 'Build Mindset', img: 'https://images.unsplash.com' },
  { id: 4, title: 'Mindful Meditation', desc: 'Clear your mind and find peace', price: 'Free', btn: 'Start Meditating', img: 'https://images.unsplash.com' },
  { id: 5, title: 'Productivity Hacks', desc: 'Maximize your day effectively', price: 'Free', btn: 'Learn More', img: 'https://img.freepik.com' }
]);
</script>

<template>
  <div class="app-wrapper">
    <header class="main-header">
      <h1>{{ message }}</h1>
    </header>

    <section class="container profile-grid">
      <div class="info-box about">
        <h2>About Me</h2>
        <p>I am <strong>{{ name }}</strong>, 19 years old.</p>
      </div>
      <div class="info-box house">
        <h2>House</h2>

        <p>San Antonio Village, Makati City.</p>
      </div>
      <div class="info-box school">
        <h2>School</h2>
        <p>Asia Pacific College</p>
      </div>
      <div class="info-box course">
        <h2>Course</h2>
        <p>BS Information Technology</p>
      </div>
      <div class="info-box hobbies">
        <h2>Hobbies</h2>
        <p>Gaming, Anime, Sports, Traveling, Workout.</p>
      </div>
    </section>

    <section class="store-section">
      <header class="store-header">
        <h2>Self Growth Store</h2>
        <p>Invest in yourself</p>
      </header>

      <div class="products-grid">
        <div v-for="item in products" :key="item.id" class="product-card">
          <div class="card-image" :style="{ backgroundImage: `url(${item.img})` }"></div>
          <div class="card-content">
            <h3>{{ item.title }}</h3>
            <p class="desc">{{ item.desc }}</p>
            <p class="price">{{ item.price }}</p>
            <button class="action-btn">{{ item.btn }}</button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style>
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
  margin-top: 30px;
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
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 30px;
  gap: 20px;
  padding: 20px;
}

.container div {
  background-color: #1f1f1f; 
  color: #fff;
  width: 280px;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.4); 
  text-align: left;
  transition: transform 0.3s ease-in-out, background-color 0.3s ease;
}

.container div:hover {
  background-color: #2c2c2c; 
  color: #fff;
  transform: translateY(-10px);
}


header {
  background: #1f1f1f;
  color: #fff;
  text-align: center;
  padding: 20px 0;
}

header h2 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

header p {
  font-size: 1.1rem;
  color: #f39c12; 
}

.products {
  display: flex;
  justify-content: center;
  gap: 20px;
  padding: 30px;
  flex-wrap: wrap;
}

.card {
  background: #1f1f1f; 
  width: 300px;
  text-align: center;
  border-radius: 10px;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
  transition: transform 0.3s ease;
  padding-bottom: 10px;
  overflow: hidden;
}

.card:hover {
  transform: translateY(-20px);
}

.image {
  height: 180px;
  background-size: cover;
  background-position: center;
  border-radius: 10px;
  align-content: center;
}

h3 {
  font-size: 1.5rem;
  color: #e74c3c; 
  margin-top: 20px;
}

.desc {
  font-size: 1rem;
  color: #bdc3c7; 
  margin-bottom: 20px;
  padding: 0 20px;
}

.price {
  color: #2ecc71; 
  font-weight: bold;
  margin-bottom: 20px;
}

button {
  padding: 10px 20px;
  background: #e74c3c; 
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s ease;
}

button:hover {
  background: #c0392b; 
}

footer {
  background-color: #1f1f1f;
  color: white;
  padding: 20px;
  text-align: center;
}

footer p {
  margin: 0;
  font-size: 1rem;
}


</style>
