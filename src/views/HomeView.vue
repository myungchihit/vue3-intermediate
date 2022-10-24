<template>
  <div>
    <h2>Home View</h2>
    <!-- $route로 라우터의 접근을 할 수 있다. -->
    <p>{{ $route.name }}</p>
    <button class="btn btn-primary" @click="goAboutPage">About으로 이동</button>
  </div>
</template>

<script setup>
import { useRouter } from 'vue-router';

const router = useRouter();
const goAboutPage = () => {
  router.push('/about');
};
</script>

<style></style>
