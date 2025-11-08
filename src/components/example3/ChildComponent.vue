<!-- ChildComponent.vue -->
<template>
  <div>
    <p>{{ message }}</p>
    <button @click="emit('custom-event', 'Hello from child')">Send Event</button>
  </div>
  </template>

<script setup lang="ts">
import { toRef } from 'vue'

const props = defineProps<{ message: string }>()
const emit = defineEmits<{ (e: 'custom-event', payload: string): void }>()

// props 구조분해 대신 toRef로 반응성 유지
const message = toRef(props, 'message')
</script>
