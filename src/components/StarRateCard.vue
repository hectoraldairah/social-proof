<template>
  <div class="card" :style="{'margin-right': margin}">
    <div class="stars">
      <img src="../assets/icon-star.svg" />
      <img src="../assets/icon-star.svg" />
      <img src="../assets/icon-star.svg" />
      <img src="../assets/icon-star.svg" />
      <img src="../assets/icon-star.svg" />
    </div>
    <div class="text">{{ msg }}</div>
  </div>
</template>

<script>
export default {
  name: 'StartRateCard',
  props: {
    msg: String,
    margin: {
      type: String,
      default: '0',
    },
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  background: $light-grayish-magenta;
  border-radius: 10px;
  padding: 1rem 0;
  margin-top: 1rem;
  .stars {
    img {
      margin: 0 4px;
    }
  }
  .text {
    margin-top: 0.5rem;
    color: $dark-magenta;
    font-weight: 700;
  }
}

@media (min-width: 1220px) {
  .card {
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 30rem;
    padding-right: 5rem;
    padding-top: 1.1rem;
    padding-bottom: 1.1rem;

    .text {
      margin: 0;
    }
  }
}
</style>
