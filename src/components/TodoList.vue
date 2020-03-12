<template>
  <div>
    <draggable
      v-model="myArray"
      group="people"
      @start="drag = true"
      @end="drag = false"
      class="flex flex-wrap"
    >
      <div
        v-for="element in myArray"
        :key="element.name"
        class="max-w-md bg-white shadow-xl m-2 px-4 py-2 rounded-lg"
      >
        {{ element.name }}
      </div>
      <button slot="footer">Button Test</button>
    </draggable>
  </div>
</template>

<script>
import draggable from 'vuedraggable'

export default {
  data: () => ({
    myArray: [
      {
        name: 'Lee',
        age: 24,
        hobby: 'computer'
      },
      {
        name: 'Jin',
        age: 64,
        hobby: 'read a book'
      },
      {
        name: 'Kim',
        age: 32,
        hobby: 'basketball'
      }
    ],
    drag: true
  }),

  components: {
    draggable
  }
}
</script>
