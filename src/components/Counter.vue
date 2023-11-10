<template>
  <h1>Counter value is: {{ value }}</h1>
  <button @click="increaseValue">Append counter value</button>
  <button @click="decreaseValue">Decrease counter value</button>
</template>

<script setup lang="ts">
import {ref} from "vue";


const props = defineProps<{ startingValue: number }>();

const value = ref(props.startingValue)

function increaseValue() {
  value.value += 1
}

function decreaseValue() {
  value.value -= 1
}
</script>