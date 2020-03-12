<template>
  <main class="px-4 mt-4 bg-gray-200 h-screen">
    <TodoList />
  </main>
</template>

<script>
export default {
  components: {
    TodoList: () => import('@/components/TodoList.vue')
  }
}
</script>
