<template>
  <div class="management">
    <div class="flex-center">
      <h2>生徒管理ページ</h2>
    </div>
    <div class="table">
      <table>
        <tr>
          <th>名前</th>
          <th>ID</th>
        </tr>
        <tr v-for="student in students" :key="student.id">
          <td>{{ student.name }}</td>
          <td>{{ student.id }}</td>
        </tr>
      </table>
    </div>
    <NuxtLink to="/" class="flex-center">戻る</NuxtLink>
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
.table {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.table td {
  padding: 3vh 5vw;
}
.flex-center {
  display: flex;
  justify-content: center;
}
</style>
