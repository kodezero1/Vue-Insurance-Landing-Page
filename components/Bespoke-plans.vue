<template>
  <Section class="mt-5 pt-4">
    <div class="row">
      <div class="col-lg-7 col-md-8 col-sm-10 m-auto text-center">
        <h4 class="tag text-success mt-lg-5 small" >Bespoke plans</h4>
        <br />

        <h1 class="display-5 fw-bold text-navy" data-aos="fade-in" data-aos-delay="300">
          Tailor-made plans suited for your business
        </h1>
        <br />
        <p class="text-muted m-auto" data-aos="fade-up" data-aos-delay="400">
          We offer flexible and innovative insurance coverage for every aspect
          of your business.
        </p>
        <br />
        <br />
      </div>

      <div class="tabs-container m-auto py-4 px-5" data-aos="zoom-in" data-aos-delay="300">
        <div class="tab-button-group mb-5">
          <div class="d-flex justify-content-center gap-4">
            <button class="btn btn-success">Auto</button>
            <button class="btn btn-light">Health</button>
            <button class="btn btn-light">Others</button>
          </div>
        </div>

        <div class="tabs-cards row justify-content-center gap-4">
          <div class="card col-sm-8 col-md-5 col-lg-3 py-4" v-for="(plan, index) in plans" :key="index">
            <div class="c-header d-flex align-items-end mb-3">
              <i class="text-success fw-bold me-3" :class="plan.icon" v-if="plan.icon"></i>
              <i class="bi bi-basket-fill text-success fw-bold me-3" v-else></i>
              <h6 class="fw- mb-0">{{plan.name}}</h6>
            </div>
            <p class="des text-muted small">
              {{plan.description}}
            </p>
            <a :href="plan.link" class="link text-navy fw-bold">
              Learn More
              <i class="bi bi-arrow-right ms-2"></i>
            </a>
          </div>

        </div>
      </div>
    </div>
  </Section>
</template>

<script>
export default {
  name: "bespokeplans",
  props: {
    plans: {
      type: Array,
      default: () => [
        {
          icon: "",
          svg: "",
          name: "Comprehensive",
          description: "Covers all the vehicle used to drive growth in your business",
          link: "",
          colour: ""
        },
        {
          icon: "",
          svg: "",
          name: "Monthly Comp. Auto",
          description: "Minimise vehicle risks with an affordable auto insurance.",
          link: "",
          colour: ""
        },
        {
          icon: "",
          svg: "",
          name: "Mini Comp. Auto",
          description: "Get your vehicles on the road without worry on your budget.",
          link: "",
          colour: ""
        },
        {
          icon: "",
          svg: "",
          name: "3rd Party Auto",
          description: "Drive with confidence while you save on insurance costs.",
          link: "",
          colour: ""
        },
      ]
    }
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
