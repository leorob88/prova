<script setup>
import { ref } from "vue";
import Btn from "./Button.vue";

defineProps({
  price: Number,
  remaining: Number
})
const quantity = ref(0)
const decrement = function (price, remaining) {
    if (quantity > 0) {
        quantity--;
        remaining += price;
    }
}
const increment = function (price, remaining) {
    if (remaining >= price) {
        quantity++;
        remaining -= price;
    }
}
</script>

<template>
  <div class="selection">
    <Btn text="-" @click="decrement" class="minus-button" />
    <div class="quantity">{{ quantity }}</div>
    <Btn text="+" @click="increment" class="plus-button" />
  </div>
</template>

<style>
.selection{
  max-width: 27%;
  padding-top: 5px;
  display: flex;
  justify-content: space-around;
}
.minus-button{
  max-width: 30%;
}
.quantity{
  color: #222;
  border: solid 1px #04c;
  border-radius: 3px;
  background-color: #cdf;
  padding-top: 3px;
  text-align: center;
}
.plus-button{
  max-width: 30%;
  padding-left: 3px;
}
</style>
