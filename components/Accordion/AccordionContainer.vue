<template>
  <div class="accordion__container">
    <div class="container">
      <AccordionItem
        v-for="(d, idx) in data"
        :selected="idx === selected"
        :accordionItem="idx"
        :key="idx"
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
  data() {
    return {
      selected: 0,
    }
  },
  props: {
    data: {
      type: Array,
      required: false,
    },
  },
  methods: {
    handleSelected(index) {
      this.selected = index === this.selected ? null : index
    },
  },
  components: { AccordionItem },
}
</script>

<style>
@media (min-width: 768px) {
  .accordion__container {
    display: none;
  }
}
</style>
