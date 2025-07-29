<script setup lang="ts">
import TodoItem from './components/molecules/Card/TodoItem.vue';

const todo: { id : string, title: string, description?: string }[] = [{
  id: '1',
  title: 'title 1',
  description: 'description 1',
}, {
  id: '2',
  title: 'title 2',
  description: 'description 2',
}, {
  id: '3',
  title: 'title 3',
  description: 'description 3',
}, {
  id: '4',
  title: 'title 4',
  description: 'description 4',
}, {
  id: '5',
  title: 'title 5',
}]

const inputValue: Ref<string> = ref<string>('');

</script>

<template>
  <div class="p-4 grid gap-4">
    <Input v-model="inputValue" />
    <Button>追加</Button>
    <div v-for="item in todo " :key="item.id">
      <TodoItem :title="item.title" :description="item.description" />
    </div>
  </div>
</template>
