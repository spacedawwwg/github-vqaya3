<script lang="ts" setup>
export interface Props {
  items: {
    id: string;
  }[];
}

defineProps<Props>();
</script>

<template>
  <template v-for="item of items">
    <div v-if="$slots && $slots[item.id]">
      <slot :name="item.id" />
    </div>
  </template>
</template>
