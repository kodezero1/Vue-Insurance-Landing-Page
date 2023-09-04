<template>
  <Section>
    <h5 class="text-muted">{{ title }}</h5>
    <br/>
    <div class="brand-container">
      <figure class="brand-figure">
        <div v-if="!Array.isArray(brands) || brands.length === 0"></div>
        <img
          v-for="(brand, index) in brands"
          :key="index"
          :src="require('../static/img/' + brand)"
          alt="brand"
          class="brands"
          v-else
        />
      </figure>
    </div>
    <br/>
  </Section>
</template>

<script>
export default {
  name: "Brands",
  props: {
    brands: {
      type: Array,
      default: () => [
        "brands/1.png",
        "brands/2.png",
        "brands/3.png",
        "brands/4.png",
        "brands/5.png",
        "brands/6.png",
        "brands/7.png",
        "brands/8.png",
        "brands/9.png",
        "brands/10.png",
        "brands/11.png",
        "brands/12.png",
        "brands/13.png",
        "brands/14.png",
        "brands/15.png",
        "brands/16.png",
      ],
    },
    title: {
      type: String,
      default: "Brands covered by us:",
    },
  },
  setup() {
    return {};
  },
};
</script>

<style scoped>
.brand-container {
  overflow: hidden;
  height: 80px;
}

.brand-figure {
  overflow: hidden;
  width: 100%;
  position: relative;
  animation: 15s cubic-bezier(0.54, 0.61, 0, 1.19) slide infinite 5s;
}

@keyframes slide {
  0% {
    top: 0;
  }

  20% {
    top: -100%;
  }
  40% {
    top: -200%;
  }
  60% {
    top: -300%;
  }
  80% {
    top: -400%;
  }
  100% {
    top: 0;
  }
  183% {
    top: -600%
  }
}

@media screen and (max-width: 650px ) {
  .brand-container {
    height: 40px;
  }

  .brand-container img {
    width: 642px
  }
}

</style>
