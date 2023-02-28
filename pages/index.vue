<template>
  <div class="onboard__screen">
    <div class="container">
      <div class="onboard__logo">
        <img
          src="https://filta.wpenginepowered.com/wp-content/themes/FiltaGlobal/assets/images/brand-logo.png"
          alt="Filta"
        />
        <img
          src="//cdn.shopify.com/s/files/1/1987/3449/t/5/assets/mindarc-logo-blk.png?v=152472296200138488861589258936"
          width="55"
          height="55"
          alt="mindarc"
          class="grayscale"
        />
      </div>

      <div class="onboard__content">
        <h1>Welcome!</h1>
        <p>Click the button on the bottom right to get started.</p>
      </div>
      <img
        src="/media/images/arrow.png"
        alt="Squiggly Arrow pointing"
        class="arrow"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>

<style>
.onboard__screen {
  height: 100vh;
  width: 100vw;
  background: #1a1a1a;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  position: relative;
  overflow-y: hidden;
}

.onboard__logo {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1em;
}

.onboard__logo .grayscale {
  -webkit-filter: invert(100%);
  filter: invert(100%);
}

.onboard__logo img {
  margin-left: 14px;
}

.onboard__content {
  text-align: center;
  color: #fff;
  letter-spacing: 0.1rem;
}

.arrow {
  position: absolute;
  -webkit-filter: invert(100%);
  filter: invert(100%);
  right: 5%;
  bottom: 0px;
}

@media (max-width: 768px) {
  .arrow {
    right: 5%;
  }
}
</style>
