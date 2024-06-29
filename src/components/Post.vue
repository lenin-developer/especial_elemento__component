<script setup lang="ts">
defineProps<{
  dataX: string;
}>();
</script>

<template>
  <h3>Page Post</h3>
  <p>prop: {{ dataX }}</p>
</template>
