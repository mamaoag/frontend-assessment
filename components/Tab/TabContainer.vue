<template>
  <div class="tab__container">
    <!-- Navigation -->
    <TabNavigation
      :headers="data"
      :selected="selected"
      @handleSelect="handleSelected"
    />
    <!-- Content -->
    <div class="tab__content_container p-4">
      <TabContent
        v-if="data.length > 0 && selected <= data.length"
        :content="data[selected].content"
      />
    </div>
  </div>
</template>

<script>
import TabContent from './TabContent.vue'
import TabNavigation from './TabNavigation.vue'

export default {
  name: 'TabContainerComponent',
  components: { TabContent, TabNavigation },
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
      this.selected = index
    },
  },
}
</script>

<style>
.tab__container {
  background: #fff;
  border-radius: 12px;
}

@media (max-width: 767.98px) {
  .tab__container {
    display: none;
  }
}
</style>
