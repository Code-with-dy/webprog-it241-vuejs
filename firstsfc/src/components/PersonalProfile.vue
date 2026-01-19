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

<style scoped>
:root {
  --primary: #42b883;
  --bg-soft: #f9f9f9;
  --text-main: #2c3e50;
  --shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
}

.app-wrapper {
  font-family: 'Inter', sans-serif;
  color: var(--text-main);
  background-color: var(--bg-soft);
  padding: 40px 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.profile-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 15px;
  margin-bottom: 50px;
}

.info-box {
  background: white;
  padding: 20px;
  border-radius: 12px;
  box-shadow: var(--shadow);
  transition: transform 0.2s ease;
}

.info-box:hover {
  transform: translateY(-5px);
}

.about { grid-column: span 2; }
.hobbies { grid-column: span 3; }

.store-header { text-align: center; margin-bottom: 30px; }

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 25px;
}

.product-card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: var(--shadow);
  display: flex;
  flex-direction: column;
}

.card-image {
  height: 180px;
  background-size: cover;
  background-position: center;
}

.card-content { padding: 20px; text-align: center; }

.action-btn {
  background: #42b883;
  color: white;
  border: none;
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 600;
  cursor: pointer;
  width: 100%;
  margin-top: 15px;
}

@media (max-width: 768px) {
  .profile-grid { grid-template-columns: 1fr; }
  .about, .hobbies { grid-column: span 1; }
}
</style>
