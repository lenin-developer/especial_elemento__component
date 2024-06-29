<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
import ComponentExample from './componentExample/ComponentExample.vue';
import ComponentAsync from './componentExample/ComponentAsync.vue';
</script>

<template>
  EL < componente > solo se puede utilizar con componetes registrados de forma
  global o importados de forma statica de forma local, pero por defecto no se
  pude utilizar para hacer un cambio dinamico de componente con componentes
  asincronos
  <HelloWorld />
  <ComponentExample />
  Nota: para que se puede realizar el cambio de componentes de forma dinamica
  con componentes asincronos se necesita que se envuelva del componente
  suspense, (por eso este ejemplo no funcion) - pero en otro stackblitz podemos
  ver el ejemplo
  <ComponentAsync />
</template>

<style scoped></style>
