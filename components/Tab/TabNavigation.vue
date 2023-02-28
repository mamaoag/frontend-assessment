<template>
  <nav class="tab__header">
    <div v-if="headers && headers.length > 0" class="tab__header_container">
      <div
        v-for="(header, idx) in headers"
        :key="idx"
        :class="{ active: selected == idx }"
        class="tab__link"
        @click="handleClick(idx)"
      >
        {{ header.title }}
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'TabNavigationComponent',
  props: {
    headers: {
      type: Array,
      required: false,
    },
    selected: {
      type: Number,
      default: 0,
    },
  },
  methods: {
    handleClick(idx) {
      this.$emit('handleSelect', idx)
    },
  },
}
</script>

<style>
.tab__header {
  border-bottom: 2px solid #f3f4f6;
}

.tab__header_container {
  display: flex;
  justify-content: space-evenly;
}

.tab__link {
  padding: 8px;
  text-align: left;
  transition: ease-in 0.2s;
  letter-spacing: 0.1rem;
  color: #64748b;
}

.tab__link:hover {
  border-bottom: 2px solid #fea706;
  font-weight: bold;
  color: #000;
}

.tab__header .active {
  border-bottom: 2px solid #fea706;
  font-weight: bold;
  color: #000;
}

.tab__link:hover {
  cursor: pointer;
}
</style>
