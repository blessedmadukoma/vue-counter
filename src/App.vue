<script setup>
import { ref } from "vue"

let count = ref(0);

const addToCount = () => {
  count.value++;
  console.log(count.value);
}

const subtractFromCount = () => {
  count.value--;
}
</script>

<!-- <script>
export default ({
  data() {
    return {
      count: 0,
    }
  },
  methods: {
    addToCount() {
      this.count.value++;
    },
    subtractFromCount() {
      this.count.value--;
    }
  }
})
</script> -->

<template>
  <main>
    <div>
      <h4>The current count is...</h4>
      <h1>{{ count }}</h1>
      <button @click="subtractFromCount">-</button>
      <button @click="addToCount">+</button>
    </div>
  </main>
</template>

<!-- <style lang="scss"> -->
<style scoped>
main {
  background-color: aliceblue;
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

div {
  text-align: center;
}
</style>