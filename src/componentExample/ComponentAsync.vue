<script setup lang="ts">
import { type Ref, ref, defineAsyncComponent } from 'vue';

const Home = defineAsyncComponent(() => import('../components/Home.vue'));
const Post = defineAsyncComponent(() => import('../components/Post.vue'));

const elementSelect: Ref<string> = ref('home');
const dataX: Ref<string> = ref('soy un dato');

const showElement = (element) => {
  elementSelect.value = element;
};
</script>

<template>
  <div>
    <button @click="showElement(home)">Home</button>
    <button @click="showElement(post)">Post</button>
  </div>
  <component
    :is="elementSelect === home ? Home : Post"
    :data-x="dataX"
  ></component>
</template>

<style scoped></style>
