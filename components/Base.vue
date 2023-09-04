<!-- Please remove this file from your project -->
<template>
  <main>
    <Navbar />
    <Header />
    <Brands />
    <Experience />
    <BespokeSolution />
    <BespokePlans />
    <Assessment />
    <Convinience />
<!--    <Brands title="Co-creating solutions with:" class="mt-5 pt-4" />-->
    <GetInTouch />
    <Footer />
  </main>
</template>

<script>
import Navbar from "./Layouts/Navbar.vue";
import BespokeSolution from "./Bespoke-solution.vue";
import BespokePlans from "./Bespoke-plans.vue";
import Assessment from "./Assessment.vue";
import Convinience from "./Convinience.vue";
import GetInTouch from "./Get-in-touch.vue";
import Footer from "./Layouts/Footer.vue";

export default {
  name: "Index",
  components: {
    Navbar,
    BespokeSolution,
    BespokePlans,
    Assessment,
    Convinience,
    GetInTouch,
    Footer,
  },
};
</script>
<style></style>
