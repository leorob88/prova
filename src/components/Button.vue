<script setup>

defineProps({
  text: String,
})
</script>

<template>
  <button>{{ text }}</button>
</template>

<style>
button{
  background-color: #642;
  width: 60px;
  border: solid #765 2px;
  border-radius: 3px;
  text-align: center;
}
button:hover{
  background-color: #864;
  color: #ccc;
}
</style>