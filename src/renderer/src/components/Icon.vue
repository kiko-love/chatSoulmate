<template>
  <span class="icon" :class="iconName">
    <svg v-if="isSvg" :class="svgClass" :style="svgStyle">
      <use :href="`${iconName}`"></use>
    </svg>
    <img v-else :src="iconName" alt="" :class="svgClass" :style="svgStyle" />
  </span>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  iconName: {
    type: String,
    required: true
  },
  className: {
    type: String,
    default: ''
  },
  style: {
    type: Object,
    default: () => ({})
  }
})

const isSvg = computed(() => props.iconName.endsWith('.svg'))
const svgClass = computed(() => `svg-icon ${props.className}`)
const svgStyle = computed(() => ({ ...props.style }))
</script>

<style lang="less">
.svg-icon {
  display: inline-block;
  width: 1em;
  height: 1em;
  vertical-align: middle;
  fill: currentColor;
}
</style>
