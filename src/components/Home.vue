<script setup lang="ts">
defineProps<{
  dataX: string;
}>();
</script>

<template>
  <h3>Page Home</h3>
  <p>prps : {{ dataX }}</p>
</template>
