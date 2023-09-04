<template>
  <Section>
    <br/>
    <div class="row flex-wrap py-4 justify-content-between align-items-center">

      <div class="col-sm-10 col-md-7 col-lg-5">
          <h1 class="display-5 fw-bold mb-3 text-navy" data-aos="fade-in" data-aos-delay="200">
            Set your <span class="effects">business</span> up for success with
            seamless insurance
          </h1>
          <p class="text-dark text-small" data-aos="fade-up" data-aos-delay="300">
            We protect all your hard work with affordable insurance to help your
            business recover from unplanned events quickly.
          </p>
        <br/>

        <p class="call-to-action">
          <button class="btn btn-success rounded-1">Get Covered</button>
        </p>
      </div>

      <div class="col-sm-8 col-lg-5 m-sm-auto m-md-0">
        <img
          src="../static/img/Property 1=Component 137.png"
          alt="header-img" class="w-100"
        />
      </div>
    </div>

  </Section>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
.effects {
  position: relative;
}

.effects::before {
  content: "";
  position: absolute;
  bottom: 6px;
  left: 0;
  width: 100%;
  height: 10px;
  background-color: #ffc107;
  z-index: -1;
}
</style>
