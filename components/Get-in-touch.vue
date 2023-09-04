<template>
  <div class="bg-success-20 my-5">
    <Section class="mt-5 py-5">
      <div class="row justify-contents-between">
        <div class="col-sm-8 col-md-8 col-lg-6">
          <h1 class="text-navy fw-bold display-5" data-aos="fade-in" data-aos-delay="300">
            What would you like to know?
          </h1>
          <br />
          <div class="btn-container mt-4 gap-3">
            <button class="btn btn-success rounded-1" type="button" data-aos="fade-up" data-aos-delay="400">
              Let's talk
            </button>
            <button class="btn btn-light" type="button" data-aos="fade-up" data-aos-delay="450">Get Started</button>
          </div>
        </div>

        <div class="col-md-8 col-sm-12 col-lg-5 mt-5" data-aos="fade-in" data-aos-delay="400">
          <ul class="list-container ps-0">
            <li
              class="list-item px-1 rounded border-bottom pt-2"
              v-for="(question, index) in questions"
              :key="index"
              :class="[question.expanded && 'bg-success-20']"
            >
              <div
                class="tag w-100 px-0 d-flex align-items-center justify-content-between py-3"
                @click="open(question, index)"
              >
                <h5 class="fw-bold mb-0">{{ question.title }}</h5>
                <i class="bi bi-caret-down p-2" v-if="!question.expanded"></i>
                <i class="bi bi-caret-up p-2" v-else></i>
              </div>

              <p class="des" :class="{ wrapped: !question.expanded }">
                <br />
                {{ question.description }}
              </p>
            </li>
          </ul>
        </div>
      </div>
    </Section>
  </div>
</template>

<script>
export default {
  props: {
    questions: {
      type: Array,
      default: () => [
        {
          title: "Are you an insurance company?",
          expanded: true,
          description:
            "Mycovergenius is Africa's first and leading insurtech platform. We are focused on expanding insurance adoption in Africa by creating unique and relevant products for anyone.",
        },
        {
          title: "How long before my plan becomes active?",
          expanded: false,
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit.Voluptatibus tenetur velit laboriosam incidunt architecto perspiciatis culpa esse perferendis deleniti sequi.",
        },
        {
          title: "How do I get covered?",
          expanded: false,
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit.Voluptatibus tenetur velit laboriosam incidunt architecto perspiciatis culpa esse perferendis deleniti sequi.",
        },
        {
          title: "Can I get a unique plan for my business?",
          expanded: false,
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit.Voluptatibus tenetur velit laboriosam incidunt architecto perspiciatis culpa esse perferendis deleniti sequi.",
        },
      ],
    },
  },
  methods: {
    open(e, i) {
      this.questions.forEach((item, index) => {
        // Close any active question
        item.expanded = false;
        if (i === index) {
          item.expanded = !item.expanded;
        }
      });
    },
  },
};
</script>

<style scoped>
.des {
  height: 150px;
  overflow: hidden;
  overflow-y: auto;
  transition: 300ms ease;
  opacity: 1;
  border-top: 1px solid var(--bs-gray-200);
  box-sizing: border-box;
}
.des.wrapped {
  height: 0;
  opacity: 0;
  padding: 0 !important;
}
.tag {
  cursor: pointer;
}
</style>
