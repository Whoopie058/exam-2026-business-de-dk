<template>
  <div class="page">
    <Header />
    <section class="hero">
      <img src="/Top-Picture.png" alt="Top Picture" />
    </section>

    <section class="content-block">
      <p>This is a placeholder text. Replace me with actual content.</p>
    </section>
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
</script>



<style scoped>
.page {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
  background: #eff0eb;
}
.hero {
  flex: 1 1 auto;
  width: 100%;
  margin: 0;
  overflow: hidden;
}
.hero img {
  width: 100%;
  height: auto;
  display: block;
}

.content-block {
  margin: 2rem;
  padding: 2rem;
  max-width: 33.333%;
  background: var(--Blue-1);
  border-radius: 0.5rem;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.content-block p {
  margin: 0;
  color: #fff;
  font-size: 1rem;
  line-height: 1.6;
}
</style>
