<template>
  <div class="container">
    <div class="options">
      <h2>生徒一覧</h2>
      <NuxtLink to="students">生徒の情報を見る</NuxtLink>
    </div>
    <div class="options">
      <h2>管理者</h2>
      <NuxtLink to="management">生徒一覧</NuxtLink>
    </div>
  </div>
</template>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.options {
  margin: 0 5vw;
}
</style>
