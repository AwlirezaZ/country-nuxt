<template>
  <component :is="tag">
    <slot/>
  </component>
</template>

<script setup>
const props = defineProps({
  tag: {
    type: String,
    default: "li",
  },
});
</script>

<style lang="scss" scoped></style>
