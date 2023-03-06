<script setup>
import ItemRow from "./ItemRow.vue";

defineProps({
  remaining: Number
})
</script>

<template>
  <div class="frame">
    Shop items:
    <ItemRow name="Potion" price=50 remaining={{remaining}} />
    <ItemRow name="Potion" price=50 remaining={{remaining}} />
    <ItemRow name="Potion" price=50 remaining={{remaining}} />
    <ItemRow name="Potion" price=50 remaining={{remaining}} />
  </div>
</template>

<style>
.frame {
    padding: 10px;
    margin: 5px auto;
    border: solid #aaa 2px;
    border-radius: 3px;
}
</style>
