<script setup>
import { reactive } from '@vue/reactivity'

const state = reactive({
  count: 0,
})

const increment = () => {
  state.count++
}

const decrement = () => {
  state.count--
}
</script>

<template>
  <div class="grid center gap-1 p-4">
    <h1 class="text-center text-3xl">{{ state.count }}</h1>
    <div class="flex justify-center gap-2">
      <button class="btn-primary" @click="increment">+ Increment</button>
      <button class="btn-danger" @click="decrement">- Decrement</button>
    </div>
  </div>
</template>
