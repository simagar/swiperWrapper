<template>
  <div class=" w-full px-2 py-2">
    <swiper
        v-bind="options"
    >
      <swiper-slide v-for="item in items" class="">
        <slot :data="item" name="slide"></slot>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script lang="ts" setup>
import type PropType from 'vue'

const props = defineProps({
  items: {
    type: Array,
    required: true
  },
  options: {
    type: Object as PropType<object>
  }
})
</script>

<style scoped>

</style>
