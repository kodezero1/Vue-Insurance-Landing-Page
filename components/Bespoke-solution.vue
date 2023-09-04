<template>
  <Section class="mt-5 py-4">
    <div class="row align-items-end justify-content-between">
      <div class="col-lg-5 col-md-8 col-sm-8 px-3">
        <h4 class="tag text-success mt-lg-5 small">Bespoke solutions</h4>
        <br/>

        <h1 class="display-5 fw-bold text-navy">
          One-in-all Solution for Business
        </h1>
        <br/>
        <p class="text-muted fw-bold" data-aos="zoom-in" data-aos-delay="300">
          We empower you with data via a web interface for managing plans and
          staff to drive better management decisions
        </p>
        <br/>
        <br/>
        <ul class="list-group">
          <li class="list-item" :class="[plan.color, plan.active && 'active']" v-for="(plan, index) in solutions.names"
              :key="plan.id" @click="select(index)"><span>{{ plan.id }}</span></li>
        </ul>
      </div>

      <div class="col-lg-6 col-md-8 col-sm-10 overflow-hidden my-5 img-wrapper" data-aos="fade-up" data-aos-delay="400"
           id="solImgContainer">
        <img
          :src="require('../static/img/solution/'+sol)"
          class="w-100 ms-5 ps-5"
          alt="Empowerment"
          v-for="(sol, index) in solutions.images"
          :key="index"
          :id="'sol-'+index"
        />
      </div>
    </div>
  </Section>
</template>

<script>
import scroll from "vue-scrollto"

export default {
  data: () => ({
    solutions: {
      names: [
        {
          id: "Plans",
          color: "purple",
          active: true
        },
        {
          id: "Claims",
          color: "orange",
          active: false
        },
        {
          id: "Beneficiaries",
          color: "success",
          active: false
        },
        {
          id: "Wallet",
          color: "success",
          active: false
        },
      ],
      images: ["plan.png", "claims.png", "benefi.png", "wallet.png"]
    },
  }),
  methods: {
    toggleImg(i) {

      //  Get Bounding images
      let solImgContainer = document.getElementById("solImgContainer")
      let solutionImages = document.getElementById(`sol-${i}`);

      //Get Bounding clients
      let bodyRect = solImgContainer.getBoundingClientRect().top;
      let imgRect = solutionImages.getBoundingClientRect().top;
      let totalOffset = (imgRect - bodyRect)
      let options = {
        container: "#solImgContainer",
        force: true,
        cancelable: true,
        x: false,
        y: true
      }
      scroll.scrollTo(solutionImages, 500, options);
    },
    select(i) {
      this.solutions.names.forEach((item, index) => {
        //Remove all the selected list
        item.active = false;

        if (index === i) {
          //Highlight item
          item.active = !item.active;
          this.toggleImg(index);
        }
      })
    }
  },

};
</script>

<style scoped>
.list-group .list-item {
  padding: 1.2rem 1rem;
  background: #fff;
  box-shadow: 0 6px 12px #0000000d;
  margin-bottom: 1rem;
  border-radius: 4px;
  border-left: 4px solid;
  opacity: 0.7;
  transition: all 400ms ease;
  cursor: pointer;
}

.list-group .list-item.purple {
  border-color: #7A5AF8;
}

.list-group .list-item.orange {
  border-color: #FCCEEE;
}

.list-group .list-item.success {
  border-color: var(--success-50);
}

.list-group .list-item:hover, .list-group .list-item.active {
  opacity: 1;
  box-shadow: 0 10px 12px #0000000d;
  color: var(--navy)
}

.img-wrapper {
  position: relative;
  height: 400px;
  scroll-behavior: smooth;
}

img {
  height: inherit;
  transition: 800ms ease;
}

@media screen and (max-width: 650px) {
  .list-group {
    display: flex;
    overflow: hidden;
    overflow-x: auto;
    width: 100%;
    flex-direction: row;
    justify-content: space-between;
  }
  .list-group .list-item {
    width: 50%;
    flex-shrink: 0;
  }
  img {
    margin: 0 auto !important;
    padding: 0 !important;
  }
}
</style>
