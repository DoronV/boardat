
<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
    <header>
        <div class="wrapper">
            <img alt="Board.at" class="logo" src="@/assets/boardat.png" />

            <nav>
                <RouterLink to="/">Home</RouterLink>
                <RouterLink to="/courses">Courses</RouterLink>
                <RouterLink to="/shops">Shops</RouterLink>
                <RouterLink to="/test-rental">Test & Rental</RouterLink>
            </nav>
        </div>
    </header>
</template>

<style scoped>

header {
  /* position: fixed; */
  top: 0;
  z-index: 1000;
}

.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 1rem;
  box-sizing: border-box;
}

.logo {
  height: 80px; /* Adjust as needed */
}

nav {
  display: flex;
  gap: 1rem;
}

.logo, nav {
  flex: 0 0 auto;
}

@media (max-width: 768px) {
  nav {
    flex-direction: column;
    align-items: flex-start;
  }
}

</style>