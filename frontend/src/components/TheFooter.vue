<template>
    <footer class="footer">
        <div class="copyright">
            &copy; {{ new Date().getFullYear() }} Board.at GmbH. All rights reserved.
        </div>
    </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.footer {
    color: yellow;
    padding: 2rem;
    text-align: center;
    margin-top: auto;
}

img {
    width: 100%;
    max-width: 600px;
    height: auto;
}
 
.copyright {
    margin-top: 1rem;
}
</style>