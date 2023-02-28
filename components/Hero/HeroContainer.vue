<template>
  <div
    class="hero__container d-flex flex-column justify-content-center align-items-center"
  >
    <div class="container-fluid mx-auto">
      <h1 class="hero__title mt-4">Hello Developer!</h1>
      <h3 class="hero__subtitle">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit
      </h3>
    </div>
    <span class="watermark">Powered by HTML.COM</span>
  </div>
</template>

<script>
export default {
  name: 'HeroComponent',
}
</script>

<style>
.hero__container {
  height: 50vh;
  position: relative;
  width: 100%;
  background: url('https://via.placeholder.com/1920x650');
  background-size: 200%;
  box-shadow: inset 0 0 0 100vh rgba(0, 0, 0, 0.35);
  background-repeat: no-repeat;
  background-position: center;
}

.hero__container > .container-fluid > h1.hero__title,
.hero__container > .container-fluid > h3.hero__subtitle {
  color: #fefefe;
  text-align: center;
}

.hero__container > .container-fluid > h1.hero__title {
  font-weight: bold;
  font-size: 3rem;
  letter-spacing: 0.04rem;
}

.hero__container > .container-fluid > h3.hero__subtitle {
  font-weight: 100;
  letter-spacing: 0.035rem;
  font-size: 2rem;
}

.watermark {
  color: #6c6c6c;
  size: 0.625rem;
  bottom: 10px;
  position: absolute;
  right: 10px;
}

@media (max-width: 767.98px) {
  .hero__container {
    background: url('https://via.placeholder.com/600x600');
    background-size: cover;
    background-position: center;
  }

  .hero__container > .container-fluid > h3.hero__subtitle {
    font-size: 1.5rem;
  }
}
</style>
