<template>
  <nav class="navbar navbar-expand-lg border-bottom shadow-sm py-3">
    <Section class="d-flex align-items-end">
      <a class="navbar-brand me-5" href="#">
        <img
          src="../../static/img/icons/logo.svg"
          alt="logo"
          highPriority="high"
        />
      </a>

      <div class="d-flex justify-contents-between navbar-wrapper flex-wrap" :class="{active: navIsActive}">
        <div
          class="navbar-list d-flex justify-contents-between align-items-end mb-0"
        >
          <ul class="col-sm-8 mb-0 nav-list">
            <li class="nav-item">
              <a href="#" class="nav-link">For Individual</a>
            </li>
            <li class="nav-item">
              <a href="#" class="nav-link">Plans</a>
            </li>
          </ul>

          <ul class="nav-list mb-0">
            <li class="nav-item">
              <a class="nav-link" href="#">Claims</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">API</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Company</a>
            </li>
          </ul>
        </div>

        <div
          class="action-btn d-flex align-items-center btn-container flex-wrap"
        >
          <a href="#" class="btn btn-light me-3">Login</a>
          <a href="#" class="btn btn-success">Get Covered</a>
        </div>
      </div>

      <button class="navbar-toggler btn ms-3" type="button" @click="toggleNav">
        <span class="bi bi-list text-success" v-if="!navIsActive"></span>
        <span class="bi bi-x-lg text-danger" v-else></span>
      </button>
    </Section>
  </nav>
</template>

<script>
import { ref } from 'vue';
    
export default {
  name: "Navbar",
    setup() {
        let navIsActive = ref(false);

        // Methods
        const toggleNav = () => {
            navIsActive.value = !navIsActive.value;
            console.log(navIsActive);
        };

    return {navIsActive, toggleNav};
    },
  
};
</script>

<style scoped>
.bg-light-50 {
  background-color: #fafafa;
}
.navbar-wrapper {
  flex: 1;
  justify-content: space-between;
  transition: 400ms ease;
  z-index: 900;
}
.navbar-wrapper .navbar-list {
  flex: auto;
}

.nav-list {
  list-style: none;
}
.nav-list li {
  display: inline-block;
  padding: 0.5rem;
}
.nav-list li:hover a {
  color: var(--bs-teal);
}
@media screen and (max-width: 990px) {
  .navbar-wrapper .nav-list {
    display: flex;
    align-items: center;
    flex: auto;
  }
  .navbar-wrapper .btn-container {
    margin-left: auto;
  }
}

@media screen and (max-width: 900px) {
    .navbar-wrapper .nav-list{
        display: block;
    }
  .navbar-wrapper {
    position: fixed;
    top: 80px;
    right: 0;
    display: block !important;
    height: 100%;
    width: 0;
    opacity: 0;
    box-sizing: border-box;
    background: var(--bs-white);
    border-left: 1px solid var(--bs-gray-200);
    padding: 3rem 0;
  }
  .navbar-wrapper .navbar-list {
    display: block !important;
  }
  .navbar-wrapper.active{
    opacity: 1;
    width: 100vw;
  }
  .nav-list li {
    display: block;
  }
  .action-btn {
    display: none !important;
  }
}
</style>
}
</style>
