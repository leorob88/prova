<script setup>
import {ref} from "vue";
import Welcome from "./components/Welcome.vue";
import ItemList from "./components/ItemList.vue";

const remaining = ref(5000);
</script>

<template>
  <div class="main">
    <Welcome />
    <ItemList remaining={{remaining}} />
  </div>
</template>

<style>
*{
  color: #aaa;
  font-family: "Verdana", "Arial", sans-serif;
  font-size: 20px;
}
div{
  width: 294px;
  text-align: left;
}
.main {
  width: 320px;
  margin-top: 24px;
}
</style>
