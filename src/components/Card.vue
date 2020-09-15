<template>
  <div class="card">
    <header class="profile">
      <img class="image" :src="require(`@/assets/${imageName}`)" />
      <div class="info">
        <h4>{{ name }}</h4>
        <p>Verified Buyer</p>
      </div>
    </header>
    <div class="text">
      <p>" {{text}} "</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    name: String,
    text: String,
    imageName: String,
  },
};
</script>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  margin: 1rem;
  padding: 2rem;
  background: $dark-magenta;
  border-radius: 10px;

  .profile {
    display: flex;
    align-items: center;
    .image {
      border-radius: 50%;
      width: 50px;
      height: 50px;
    }
    .info {
      margin-left: 1rem;
      h4 {
        margin: 0;
        color: $white;
      }
      p {
        margin: 5px 0;
        color: $soft-pink;
        font-weight: 400;
      }
    }
  }

  .text {
    color: $white;
    font-weight: 400;
    line-height: 1.8rem;
  }
}

@media (min-width: 1440px) {
  .card {
    margin: 0 1rem;
    height: 12rem;
    width: 25rem;
  }
}
</style>
