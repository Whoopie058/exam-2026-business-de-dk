<template>
  <div class="page">
    <Header />
    <section class="hero">
      <img src="/Top-Picture.png" alt="Top Picture" />
    </section>

    <section class="content-block">
      <p>This is a placeholder text. Replace me with actual content.</p>
    </section>

    <section class="text-block">
      <p>Business DE-DK arbejder for at forbedre samarbejdet mellem virksomheder, institutioner og initiativer i den nordtyske og syddanske grænseregion. Projektet fokuserer på at optimere erhvervssamarbejdet, tackle manglen på arbejdskraft og gøre regionen mere attraktiv for både virksomheder og talent fra hele verden.</p>
      <h2>DE-DK Business</h2>
      <p>Data og indsigt – Kortlægning af regionens muligheder, behov og initiativer
        Netværk – Etablering af et cross-border business-netværk for erhvervsfolk og eksperter
        Synlighed – Formidling af viden og analyser via en mediekanal
        Erhvervsråd – Undersøgelse af potentialet for et cross-border business-råd
        Arbejdskraft og vækst – Tiltrækning og fastholdelse af talent i regionen
        Business DE-DK skaber overblik, faciliterer samarbejde og styrker den grænseoverskridende erhvervsudvikling.</p>
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
  margin: 4rem;
  padding: 2rem;
  max-width: 33.333%;
  background: var(--Blue-1);
  box-shadow: 10px 10px 0 #415A77;
}

.content-block p {
  margin: 0;
  color: #fff;
  font-size: 1rem;
  line-height: 1.6;
}

.text-block {
  margin: 2rem 2rem 2rem 4rem;
  padding: 2rem 2rem 2rem 0;
  max-width: calc(33.333% + 20px);
}

.text-block p {
  margin: 0;
  color: #2f3d4f;
  font-size: 1rem;
  line-height: 1.6;
}

.text-block h2 {
  margin: 1rem 0 0 0;
  color: #2f3d4f;
  font-size: 1.5rem;
}
</style>
