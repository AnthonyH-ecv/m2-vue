<template>
  <div
    class="star" :style="style"/>
</template>

<script>
import { randomX, randomY } from "../helpers/random";
export default {
    name: "Star",
    computed: {
        getRandomX() {
        return randomX();
        },
        getRandomY() {
        return randomY();
        },
        getRandomRadius() {
            return Math.round(Math.random() * Math.round(4))
        },
        style() {
            return `
                top: ${this.getRandomY}px;
                left: ${this.getRandomX}px;
                height: ${this.getRandomRadius}px;
                width: ${this.getRandomRadius}px;
            `
        }
    }
    }
</script>

<style>
.star {
  position: absolute;
  background-color: white;
  border-radius: 100%;
  height: 4px;
  width: 4px;
}
</style>