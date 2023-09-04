<template>
  <Section>
    <div class="row justify-content-between align-items-center">
      <div class="col-sm-7 col-lg-4 ">
        <div class="logo-section my-5">
          <img
            src="../../static/img/icons/logo.svg"
            alt="mycovergenius"
            style="height: 40px"
          />
        </div>
        <ul class="list-container ps-0">
          <li class="list-item py-3">
            <span class="fw-bold">Office: </span>
            <span>8, Province Estate, Maruwa Bus-Stop, Lekki Phase 1</span>
          </li>

          <li class="list-item py-3">
            <span class="fw-bold">Email: </span>
            <a href="mailto:hello@mycovergenius.com" class="text-dark"
              >hello@mycovergenius.com</a
            >
          </li>

          <li class="list-item py-3">
            <span class="fw-bold">Phone: </span>
            <a href="tel:8+2348099988005" class="text-dark">8+2348099988005</a>
          </li>

          <li class="list-item py-3 d-flex align-items-center">
            <a href="#" class="social-icon btn bi bi-facebook"></a>
            <a href="#" class="social-icon btn bi bi-instagram"></a>
            <a href="#" class="social-icon btn bi bi-linkedin"></a>
            <a href="#" class="social-icon btn bi bi-twitter"></a>
          </li>
        </ul>
      </div>

      <div
        class="col-sm-7 col-lg-7 d-flex align-items-start justify-content-between gap-4 flex-wrap"
      >
        <div class="column">
          <h5 class="text-dark fw-bold">Quick Links</h5>
          <ul class="list-container mt-4 ps-0">
            <li class="list-item mb-3"><a href="#" class="text-muted no-line">Home</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">FAQs</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Sign Up/Login</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">News</a></li>
          </ul>
        </div>
        <div class="column">
          <h5 class="text-dark fw-bold">Products</h5>
          <ul class="list-container mt-4 ps-0">
            <li class="list-item mb-3"><a href="#" class="text-muted no-line">Health Cover</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Auto Cover</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Travel Cover</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Gadget Cover</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Office Content</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Delivery Cover</a></li>
          </ul>
        </div>
        <div class="column">
          <h5 class="text-dark fw-bold">Company</h5>
          <ul class="list-container mt-4 ps-0">
            <li class="list-item mb-3"><a href="#" class="text-muted no-line">About Us</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Resources</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">For Individuals</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">API</a></li>
          </ul>
        </div>
        <div class="column">
          <h5 class="text-dark fw-bold">Legal</h5>
          <ul class="list-container mt-4 ps-0">
            <li class="list-item mb-3"><a href="#" class="text-muted no-line">Privacy Policy</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Cookies Policy</a></li>
            <li class="list-item mb-3"><a href="#" class="text-muted no-line pb-2">Terms & Conditions</a></li>
          </ul>
        </div>
      </div>
      <div class="col-12 small text-muted py-4">
        mycovergenius © 2022 / ALL RIGHTS RESERVED
      </div>
    </div>
  </Section>
</template>

<script>
import Section from "../Section.vue";
export default {
  name: "Footer",
  components: { Section },
};
</script>

<style lang="scss" scoped></style>
