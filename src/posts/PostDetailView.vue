<template>
  <div>
    <h2>제목</h2>
    <p>내용</p>
    <p class="text-muted"></p>
    <hr class="my-4" />
    <div class="row g-2">
      <div class="col-auto">
        <button class="btn btn-outline-dark">이전글</button>
      </div>
      <div class="col-auto">
        <button class="btn btn-outline-dark">다음글</button>
      </div>

      <div class="col-auto me-auto"></div>

      <div class="col-auto">
        <button class="btn btn-outline-dark" @click="goListPage">목록</button>
      </div>
      <div class="col-auto">
        <button class="btn btn-outline-primary" @click="goEditPage">
          수정
        </button>
      </div>
      <div class="col-auto">
        <button class="btn btn-outline-danger">삭제</button>
      </div>
    </div>
    <!-- 
      <p>{{ $route.params }}</p>
      url뒤에 ?: query , #: hash
      query 가져오기 query.[key]쓰면 value값만 출력
      <p>{{ $route.query.userName }}</p>
      hash 가져오기
      <p>{{ $route.hash }}</p>
    -->
  </div>
</template>

<script setup>
import { useRoute, useRouter } from 'vue-router';

const router = useRouter();
const route = useRoute();
const id = route.params.id;

const goListPage = () => {
  router.push({
    name: 'PostList',
  });
};

const goEditPage = () => {
  router.push({
    name: 'PostEdit',
    params: {
      id,
    },
  });
};
</script>

<style></style>
