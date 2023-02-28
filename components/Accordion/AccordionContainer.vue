<template>
  <div class="accordion__container">
    <div class="container">
      <AccordionItem
        v-for="(d, idx) in data"
        :key="idx"
        :selected="idx === selected"
        :accordion-item="idx"
        :title="d.title"
        :content="d.content"
        @handleSelect="handleSelected"
      />
    </div>
  </div>
</template>

<script>
import AccordionItem from './AccordionItem.vue'

export default {
  name: 'AccordionContainerComponent',
  components: { AccordionItem },
  props: {
    data: {
      type: Array,
      required: false,
    },
  },
  data() {
    return {
      selected: 0,
    }
  },
  methods: {
    handleSelected(index) {
      this.selected = index === this.selected ? null : index
    },
  },
}
</script>

<style>
@media (min-width: 768px) {
  .accordion__container {
    display: none;
  }
}
</style>
