<template>
  <div class="parent__content">
    <Nuxt />
    <MenuButton />
  </div>
</template>

<script>
import MenuButton from '../components/Navigation/Menu.vue'

export default {
  components: { MenuButton },
}
</script>
<style>
.parent__content {
  position: relative;
}
</style>
