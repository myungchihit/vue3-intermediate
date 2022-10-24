<template>
  <div>
    <h2>About View</h2>
    <p>{{ $route.path }}</p>
    <button class="btn btn-primary" @click="$router.push('/')">
      Home으로 이동
    </button>
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router';

// template $route 처럼 setup에서도 useRoute를 사용하면 route에 접근이 가능하다.
// useRoute랑 useRouter랑 햇갈리지 말자
const route = useRoute();
console.log('route.path: ', route.path);
</script>

<style></style>
