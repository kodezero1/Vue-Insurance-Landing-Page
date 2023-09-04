<template>
  <div class="bg-success-20 slant py-4 my-5">
    <br />
    <br />
    <Section class="mt-5 py-4">
      <div class="row align-items-end justify-content-between">
        <div class="col-lg-5 col-md-8 col-sm-8 px-3">
          <h4 class="tag text-success mt-lg-5 small">100% claims assessment</h4>
          <br />

          <h1 class="display-5 fw-bold text-navy" data-aos="fade-in" data-aos-delay="300">
            Make claims with ease
          </h1>
          <br />
          <p class="text-muted fw-bold" data-aos="fade-up" data-aos-delay="500">
            Our digital self-inspection process lets your team report issues in real-time
            keep your business running non-stop.
          </p>
          <br />
          <br />
          <ul class="list-container sm-flex">
            <li
              class="list-item"
              v-for="(list, index) in assesment.list"
              :key="list.id"
              :class="{ selected: list.active }"
              @click="select(index)"
            >
              <div class="ps-3">
                <h6 class="fw-bold">{{ list.id }}</h6>
                <p class="des small text-muted" v-if="list.description && list.active">
                  {{ list.description }}
                </p>
              </div>
            </li>
          </ul>
        </div>

        <div class="col-lg-4 col-md-8 col-sm-10 overflow-hidden my-5" >
          <div class="img-thumbnail-circle" id="asses-img">
            <img
              :src="require('../static/img/assesment/' + item)"
              alt="assessment"
              v-for="(item, index) in assesment.images"
              :key="index"
              :id="'asses-'+index"
              class="asses-img"
            />
          </div>
        </div>
      </div>
    </Section>
  </div>
</template>

<script>
import Section from "./Section.vue";
import scroll from "vue-scrollto";

export default {
  components: { Section },
  data: () => ({
    assesment: {
      list: [
        {
          id: "Report claim",
          active: true,
          description: "It all starts with a click. Log in to your account, from any device.",
        },
        {
          id: "Take Picture",
          active: false,
          description: "Then it gets easier. Take live pictures of the damages, right from the device.",
        },
        {
          id: "Estimate damage",
          active: false,
          description: "Give us an amount it would take to fix your damages, an estimate of repairs.",
        },
        {
          id: "Get paid",
          active: false,
          description: "The sweet part. Your business gets compensated once claim is approved.",
        },
      ],
      images: ["get-paid.png", "picture.png", "damage.png", "report-calm.png"],
    },
  }),
  methods: {
    toggleImg(i) {
      //  Get Bounding images
      let Img = document.getElementById(`asses-${i}`);
      let options = {
        container: "#asses-img",
        force: true,
        cancelable: true,
        x: false,
        y: true,
      };
      scroll.scrollTo(Img, 500, options);
    },
    select(i) {
      this.assesment.list.forEach((item, index) => {
        //Remove all the selected list
        item.active = false;

        if (index === i) {
          //Highlight item
          item.active = !item.active;
          console.log(index);
          this.toggleImg(index);
        }
      });
    },
  },
};
</script>

<style scoped>
.img-thumbnail-circle {
  height: 400px;
  width: 400px;
  border-radius: 50%;
  background-color: var(--success-50);
  overflow: hidden;
  display: flex;
  align-items: center;
  padding-top: 5rem;
  box-sizing: border-box;
  gap: 3rem;
  flex-direction: column;
}
.asses-img{
  height: 400px;

}
.list-container .list-item {
  padding: 0.1rem 0.4rem;
  border-left: 3px dashed var(--bs-gray-300);
  list-style: none;
  margin-bottom: 1rem;
  cursor: pointer;
}
.list-container .list-item.selected {
  border-left-style: solid !important;
  border-color: var(--bs-indigo);
}
.list-container .list-item:not(.selected) {
  padding: 1.5rem 0.5rem;
}
.slant {
  position: relative;
  overflow: hidden;
}
.slant::before {
  content: "";
  position: absolute;
  top: -90px;
  height: 203px;
  width: 100vw;
  background-color: var(--bs-white);
  transform: rotateZ(7deg);
  border-bottom: 3px solid var(--success-50);
  box-sizing: border-box;
}
@media only screen and (max-width: 650px) {
  .sm-flex{
    display: flex !important;
    align-items: center;
    justify-content: space-between;
    flex: 100%;
  }
    .list-container .list-item {
      flex-shrink: 0 !important;
      flex: 40%;
    }
  .list-container .list-item .des{
    display: none;
  }
  .img-thumbnail-circle{
    margin: auto !important;
  }
}
</style>
