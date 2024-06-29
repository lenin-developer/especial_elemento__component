<script setup lang="ts">
import { type Ref, ref, shallowRef } from 'vue';

import Home from '../components/Home.vue';
import Post from '../components/Post.vue';

const elementSelect: Ref<string> = ref('Home');
const dataX: Ref<string> = ref('soy un dato');

const compoentes = {
  Home,
  Post,
};

const showHome = () => {
  elementSelect.value = 'Home';
};

const showPost = () => {
  elementSelect.value = 'Post';
};
</script>

<template>
  <div>
    <button @click="showHome">Home</button>
    <button @click="showPost">Post</button>
  </div>
  <component :is="compoentes[elementSelect]" :data-x="dataX"></component>
</template>

<style scoped></style>
