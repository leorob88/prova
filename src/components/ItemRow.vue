<script setup>
import Selection from "./Selection.vue";

defineProps({
  name: String,
  price: Number,
  remaining: Number
})
</script>

<template>
    <div class="item-row">
        <div style="max-width: 46%">
            <img src="../assets/potion.png" alt="img" />{{ name }}
        </div>
        <div class="price">{{ price }} Gil</div>
        <Selection price={{price}} remaining={{remaining}} />
    </div>
</template>

<style>
.item-row {
    display: flex;
    justify-content: space-between;
    font-size: 16px;
}
.price {
    padding-top: 8px;
    max-width: 26%;
}
</style>
