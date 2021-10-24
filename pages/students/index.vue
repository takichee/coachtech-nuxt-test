<template>
  <div class="container">
    <h2 class="flex-center">生徒一覧</h2>
    <ul class="students">
      <li v-for="student in students" :key="student.id">
        <NuxtLink :to="`students/${student.id}`">
          {{ student.name }}
        </NuxtLink>
      </li>
    </ul>
    <nuxt-link to="/">戻る</nuxt-link>
  </div>
</template>

<script>
export default {
  data () {
    return {
      students: [
        {
          id: 'qnfungqxllc3m1ak',
          name: '生徒A'
        },
        {
          id: '7j9cumkgsq6l264c',
          name: '生徒B'
        },
        {
          id: 'eo34bhey9m0d92ou',
          name: '生徒C'
        }
      ]
    }
  }
}
</script>

<style>
.flex-center {
  display: flex;
  justify-content: center;
}
.students {
  list-style: none;
  margin: 0 auto;
  text-align: center;
  max-width: 20vw;
}
</style>
