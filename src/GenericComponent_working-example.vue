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
/**
 * When using `defineModel` Generic type T cannot be used, else the props above won't be recognized
 */
const modelValue = defineModel<string>();
</script>

<style scoped lang="scss"></style>
