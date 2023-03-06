<script setup>

defineProps({
  remaining: Number
})
let gil = "";
if (remaining < 5000) {`Gil: 5000 > ${remaining}`} else {gil = `Gil: 5000`};
</script>

<template>
  <div class="frame">
    {{ gil }}
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