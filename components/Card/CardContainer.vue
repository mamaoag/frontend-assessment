<template>
  <div class="card__container container-fluid mt-4">
    <Card v-for="(content, idx) in contents" :key="idx" :content="content" />
  </div>
</template>

<script>
import Card from './Card.vue'

export default {
  name: 'CardContainerComponent',
  components: { Card },
  data() {
    return {
      contents: [
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco.',
      ],
    }
  },
}
</script>

<style>
.card__container {
  display: flex;
  justify-content: center;
  align-items: stretch;
}

@media (max-width: 767.98px) {
  .card__container {
    display: block;
  }
}
</style>
