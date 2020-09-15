<template>
  <div class="container">
    <div class="hero">
      <h1 class="hero__title">10,000+ of our users love our products.</h1>
      <p class="hero__text">
        We only provide great products combined with excellent customer service. See what out
        satisfied customers are saying about our services.
      </p>
    </div>
    <div class="cards">
      <StartRateCard msg="Rated 5 Stars in Reviews" />
      <StartRateCard msg="Rated 5 Stars in Report Guru" />
      <StartRateCard msg="Rated 5 Stars in BestTech" />
    </div>
  </div>
</template>

<script>
import StartRateCard from './StarRateCard.vue';

export default {
  name: 'Hero',
  components: { StartRateCard },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  padding: 0 1rem;
}

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin-top: 3rem;

  .hero__title {
    font-size: 2.2rem;
    font-weight: 700;
    margin: 20px 0;
    color: $dark-magenta;
  }

  .hero__text {
    line-height: 1.5rem;
    font-size: 1rem;
    margin: 0;
    color: $dark-grayish-magenta;
    font-weight: 500;
  }
}
.cards {
  margin-top: 3rem;
}

@media (min-width: 1440px) {
  .container {
    flex-direction: row;
    justify-content: space-between;
    padding: 1.3rem 0;
  }

  .hero {
    text-align: left;

    .hero__title {
      font-size: 3rem;
      max-width: 30rem;
      margin-left: -2rem;
    }

    .hero__text {
      max-width: 32rem;
    }
  }

  .cards {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    margin-top: 5rem;
    width: 45rem;
    :nth-child(1) {
      align-self: flex-start;
    }
    :nth-child(2) {
      align-self: center;
    }
  }
}
</style>
