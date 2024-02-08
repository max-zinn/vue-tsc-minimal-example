<template>
  <ul>
    <li v-for="item of items" :key="`${item}`">
      {{ item }}
    </li>
  </ul>
</template>
<script setup lang="ts" generic="T">
interface Props {
  items: T[];
}

const props = withDefaults(defineProps<Props>(), {
  items: () => [],
});
const modelValue = defineModel<T>();
</script>

<style scoped lang="scss"></style>
