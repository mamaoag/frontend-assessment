<template>
  <div class="menu">
    <a class="menu__button" @click="handleClick">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
      >
        <path
          v-if="!menuOpen"
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M3.75 5.25h16.5m-16.5 4.5h16.5m-16.5 4.5h16.5m-16.5 4.5h16.5"
        />
        <path
          v-else
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M6 18L18 6M6 6l12 12"
        />
      </svg>
    </a>
    <div v-if="menuOpen" class="menu__options">
      <div class="menu__header">
        Menu
        <div class="menu__links">
          <div>
            <NuxtLink to="/" @click.prevent="handleClick">Home</NuxtLink>
          </div>
          <div>
            <NuxtLink to="/exercise-1" @click.prevent="handleClick"
              >Exercise 1</NuxtLink
            >
          </div>
          <div>
            <NuxtLink to="/exercise-2" @click.prevent ="handleClick"
              >Exercise 2</NuxtLink
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MenuComponent',
  data() {
    return {
      menuOpen: false,
    }
  },
  methods: {
    handleClick() {
      this.menuOpen = !this.menuOpen
    },
  },
}
</script>

<style>
.menu a.menu__button {
  position: fixed;
  background: #111;
  right: 2%;
  bottom: 5%;
  padding: 2rem;
  border-radius: 50%;
  border: 0;
  height: 40px;
  width: 40px;
  transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.2s;
}

.menu svg {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  height: 30px;
  width: 30px;
  stroke: #fff;
  transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.2s;
}

.menu a.menu__button:hover {
  background: #fea706;
  cursor: pointer;
}

.menu a.menu__button:hover > svg {
  stroke: #111;
}

.menu .menu__options {
  position: fixed;
  display: block;
  right: 2%;
  bottom: 15%;
  padding: 2em;
  width: 10vw;
  background: #111;
  height: 20vh;
  border-radius: 12px;
  color: #fff;
  letter-spacing: 0.06rem;
}

.menu__links a {
  color: #fff;
  transition: cubic-bezier(0.075, 0.82, 0.165, 1) 0.2s;
}

.menu__links a:hover {
  color: #fea706;
}

@media (max-width: 767.98px) {
  .menu .menu__options {
    width: 50vw;
  }
}
</style>
