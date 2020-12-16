<template>
  <header>
    <div class="container">
      <nav class="navbar">
        <div class="logo">
          <img src="../assets/logo.svg" alt="logo">
        </div>
        <ul>
          <nav-button @click="toggleModal">Kontacts</nav-button>
        </ul>
      </nav>
    </div>
  </header>
  <div v-if="modalVisibility" class="modal" :class="{'background-black': mozilla}"
       @click="modalVisibility=!modalVisibility">
    <div class="modal-card">
      <p>Координаты для организаторов концертов:</p>
      <p>+7-953-748-91-32</p>
      <p>amaday82@gmail.com</p>
    </div>
  </div>
</template>

<script>
import NavButton from "@/components/NavButton";

export default {
  name: "header",
  components: {NavButton},
  data() {
    return {
      modalVisibility: false,
      mozilla: false
    }
  },
  methods: {
    toggleModal() {
      this.mozilla = this.isMozilla() ? true : false;
      this.modalVisibility = !this.modalVisibility;
    },
    isMozilla() {
      return window.navigator.userAgent.includes('Firefox');
    }
  }
}
</script>

<style scoped>
header {
  border-bottom: 1px solid yellow;
}

.logo {
  width: 80px;
  height: 80px;
  border: 1px solid yellow;
}

.logo img {
  width: 100%;
}

.logo:hover * {
  box-shadow: 0 0 5px 1px yellow;
  text-shadow: 0 0 3px white;
  cursor: pointer;
  color: white;
}

.navbar {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

ul {
  list-style: none;
}

.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.8);
  -webkit-backdrop-filter: blur(10px);
  backdrop-filter: blur(5px);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
}

.background-black {
  background-color: #000;
}

.modal-card {
  border: 1px solid yellow;
  /*width: 400px;*/
  padding: 1rem;
}
</style>
