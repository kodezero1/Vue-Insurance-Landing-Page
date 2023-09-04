<template>
  <Section class="rows my-5 pt-4">
    <h1 class="display-5 col-sm-9 m-auto text-navy text-center fw-bold">
      Experience all-around insurance for SME, startup or large business.
    </h1>
    <p class="text-center mt-4 text-dark">
      We enable every kind business grow with genuine insurance coverage.
    </p>
    <br />

    <div class="services-column mt-5 gap-4 px-3 row align-items-center">
      <div
        class="column col-md-3 col-lg-3 mb-5 col-sm-10"
        data-aos="fade-up"
        data-aos-delay="300"
      >
        <div class="column-icon-bar mb-4">
          <img src="../static/img/icons/afford.png" alt="money">
        </div>

        <h6 class="fw-semibold tag mb-3 text-navy">Affordable</h6>
        <p class=" description small">
          Get affordable insurance coverage that fits your budget.
        </p>
      </div>

      <div
        class="column col-md-3 col-lg-3 col-sm-10 mb-5"
        data-aos="fade-up"
        data-aos-delay="400"
      >
        <div class="column-icon-bar mb-4">
          <img src="../static/img/icons/paper.png" alt="paper work">
        </div>
        <h6 class="fw-semibold text-navy tag mb-3">No paperwork</h6>
        <p class="description small">
          We are online! Get your business covered without leaving your home or
          filling out long forms.
        </p>
      </div>

      <div
        class="column col-md-3 col-lg-3 col-sm-10 mb-5"
        data-aos="fade-up"
        data-aos-delay="500"
      >
        <div class="column-icon-bar mb-4">
          <img src="../static/img/icons/value.png" alt="value">
        </div>
        <h6 class="fw-semibold tag mb-3 text-navy">Added Business Value</h6>
        <p class="description small">
          Focus on your KPIs while we worry about your business risks and your
          staff.
        </p>
      </div>
    </div>
  </Section>
</template>

<script>
export default {
  name: "experience",
  props: {
    services: Array,
  },
  setup() {
    return {};
  },
};
</script>

<style scoped>
.column {
  position: relative;
}
.column .column-icon-bar {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #0000ff1f;
  color: #0000fffd;
  line-height: 50px;
  text-align: center;
  margin-bottom: 1rem;
}
.column:last-child .column-icon-bar {
  background-color: #fce7f6;
  color: #ee46bc;
}
</style>
