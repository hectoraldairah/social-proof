<template>
  <div id="app">
    <div class="bg-top"></div>
    <div class="bg-bottom"></div>
    <div class="layout">
      <div class="container">
        <section class="top">
          <Hero />
        </section>
        <section class="bottom">
          <Card
            text="We needed the same printed design as the one we had ordered a week prior.
            Not only did they find the original order, but we also received it in time.
            Excellent!"
            name="Colton Smith"
            margin="0"
            imageName="image-colton.jpg"
          />
          <Card
            text="Customer service is always excellent and very quick turn around.
            Completely delighted with the simplicity of the purchase and the speed of delivery."
            name="Irene Roberts"
            margin="2rem"
            imageName="image-irene.jpg"
          />
          <Card
            text="Put an order with this company and can only
            praise them for the very high standard.
            Will definitely use them again and recommend them to everyone!"
            name="Anne Wallace"
            margin="4rem"
            imageName="image-anne.jpg"
          />
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import Hero from './components/Hero.vue';
import Card from './components/Card.vue';

export default {
  name: 'App',
  components: {
    Hero,
    Card,
  },
};
</script>

<style lang="scss">
* {
  text-decoration: none;
}

#app {
  height: 100%;
  overflow: auto;
  position: relative;
}

.bg-top {
  position: fixed;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  background: url('./assets/bg-pattern-top-mobile.svg') no-repeat left top;
  z-index: -99;
  overflow: auto;
}

.bg-bottom {
  position: fixed;
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  background: url('./assets/bg-pattern-bottom-mobile.svg') no-repeat right bottom;
  z-index: -99;
  overflow: auto;
}

.layout {
  margin: 0 auto;
  max-width: 375px;
}

.bottom {
  display: flex;
  flex-direction: column;
  margin-top: 5rem;
}

@media (min-width: 1220px) {
  .layout {
    max-width: 1220px;
  }
}

@media (min-width: 1220px) {
  .layout {
    max-width: 1220px;
    margin: 0 auto;
  }

  .bg-top {
    background: url('./assets/bg-pattern-top-desktop.svg') no-repeat left top;
  }

  .bg-bottom {
    background: url('./assets/bg-pattern-bottom-desktop.svg') no-repeat right bottom;
  }

  .bottom {
    flex-direction: row;
    justify-content: space-between;
    height: 20rem;
    :nth-child(1) {
      align-self: flex-start;
      margin-left: 0 !important;
    }
    :nth-child(2) {
      align-self: center;
    }
    :nth-child(3) {
      align-self: flex-end;
      margin-right: 0 !important;
    }
  }
}
</style>
