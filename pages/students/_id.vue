<template>
  <div class='student_id'>
    <h2>{{ student.name }}</h2>
    <NuxtLink to="../students">生徒一覧へ戻る</NuxtLink>
    <span> | </span>
    <NuxtLink to="/">トップページへ</NuxtLink>
  </div>
</template>

<script>
export default {
  validate ({ params }) {
    return true
  },
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
  },
  computed: {
    student () {
      return this.students.find(student => student.id === this.$route.params.id)
    }
  }
}
</script>

<style>
.student_id {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
