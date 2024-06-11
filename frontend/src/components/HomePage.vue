<script setup lang="ts">

</script>

<template>
  <div class="homepage">
    <h1>Shred to Success: Ride the Peak of Performance with Board.at!</h1>
    <h2>Join Our Expert Instructors for an Unforgettable Snowboarding Experience!</h2>
    <button class="cta-button">Get Started</button>

    <div class="grid">
      <RouterLink to="/courses">
        <div class="grid-item">
          <img src="../assets/courses.jpg" alt="Courses" />
          Courses
        </div>
      </RouterLink>
      <RouterLink to="/shops">
        <div class="grid-item">
          <img src="../assets/shop.jpg" alt="Shops" />
          Shops
        </div>
      </RouterLink>
      <RouterLink to="/test-rental">
        <div class="grid-item">
          <img src="../assets/test.jpg" alt="Test" />
          Test
        </div>
      </RouterLink>
      <RouterLink to="/test-rental">
        <div class="grid-item">
          <img src="../assets/Rental.jpg" alt="Rental" />
          Rental
        </div>
      </RouterLink>

    </div>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.homepage {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.cta-button {
  background-color: #007BFF;
  /* Change to your preferred color */
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  font-size: 1.2rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
  margin-top: 20px;
}

.cta-button:hover {
  background-color: #0056b3;
  /* Darker shade for hover effect */
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  margin-top: 20px;
}

.grid-item {
  background-color: #fafafa;
  padding: 20px;
  border: 2px solid #333;
  border-radius: 5px;
  text-align: center;
  color: #333;
}

.grid-item img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 5px;
  margin-bottom: 10px;
}

@media (min-width: 1024px) {

  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
