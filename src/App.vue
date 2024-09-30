<template>
  <AppHeader />
  <AppFilters />


  <main class="app-main">
    <AppTodoList />
    <AppAddTodo @add-todo="addTodo"/>

  </main>

  <AppFooter />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import AppHeader from './components/AppHeader.vue';
import AppFilters from './components/AppFilters.vue';
import AppTodoList from './components/AppTodoList.vue';
import AppAddTodo from './components/AppAddTodo.vue';
import AppFooter from './components/AppFooter.vue';
import { Todo } from './types/todo'

export default defineComponent({
  components: {
    AppHeader,
    AppFilters,
    AppTodoList,
    AppAddTodo,
    AppFooter
  },
  methods: {
    addTodo(todo: Todo) {
      console.log(todo);
    }
  }
})
</script>
