<template>
  <Section class="mt-5 pt-4">
    <div class="row">
      <div class="col-s rounded-3 bg-navy m-auto shadow p-5">
        <div class="cad-header col-md-6">
          <p class="tag text-success small">
            Get insurance at your conveneince
          </p>
          <br />

          <h1 class="display-5 fw-bold text-white" data-aos="zoom-in" >
            Get your business covered from anywhere
          </h1>
          <br />
          <p class="text-muted"  data-aos="fade-in" data-aos-delay="100">
            Mycovergenius is making insurance in Nigeria affordable, easy and
            accessible to everyone. Get covered from any of our multiple sales
            channels.
          </p>
          <br />
        </div>
        <div class="cad-body row mt-5 justify-content-between">
          <div class="col-sm-8 col-md-6">
            <ul class="list-container ps-0">
              <li class="list-item d-flex align-items-start mb-5" data-aos="fade-up" data-aos-delay="300">
                <div class="icon">
                  <i class="bi bi-display-fill"></i>
                </div>

                <div class="text">
                  <h6 class="text-white">Via our web portal</h6>
                  <p class="text-muted">
                    Conveniently manage all our business plans and staff from
                    our web portal.
                  </p>
                  <a href="#" class="link text-sucess no-line">
                    Get covered now <i class="bi bi-arrow-right ms-3"></i>
                  </a>
                </div>
              </li>
              <li class="list-item d-flex align-items-start" data-aos="fade-up" data-aos-delay="400">
                <div class="icon">
                  <i class="bi bi-phone-vibrate-fill"></i>
                </div>

                <div class="text">
                  <h6 class="text-white">Via our Mobile App</h6>
                  <p class="text-muted">
                    Your staff also enjoys the coverage from our user-friendly
                    mobile app.
                  </p>
                  <a href="#" class="link text-sucess no-line">
                    See the app <i class="bi bi-arrow-right ms-3"></i>
                  </a>
                </div>
              </li>
            </ul>
          </div>

          <div class="col-sm-10 col-md-4 py-5" data-aos="fade-up" data-aos-delay="600">
            <img src="../static/img/convenience.png" alt="team" class="w-100">
          </div>
        </div>
      </div>
    </div>
  </Section>
</template>

<script>
import Section from "./Section.vue";
export default {
  setup() {
    return {};
  },
  components: { Section },
};
</script>

<style scoped>
.list-container .list-item .icon {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  margin-right: 0.8rem;
  background-color: var(--bs-gray-800);
  flex-shrink: 0;
  line-height: 70px;
  text-align: center;
  color: var(--success);
  font-size: 1.2em;
}
</style>
