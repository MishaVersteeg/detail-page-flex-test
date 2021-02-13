<template>
  <div class="flex-item">
    <div>{{ randomNumber }}</div>
    <div>{{ randomWord }}</div>
  </div>
</template>

<script>
const randomWords = require("random-words");
const pluralize = require("pluralize");

export default {
  computed: {
    randomNumber: () => Math.floor(Math.random() * 10000),
    randomWord: () => pluralize(randomWords()),
  },
};
</script>

<style scoped>
.flex-item {
  height: 100%;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  padding: 1rem 0.5rem;

  box-sizing: border-box;
  border-right: 0.2rem solid rgb(245, 242, 240);;
  border-bottom: 0.2rem solid rgb(245, 242, 240);;
}
.flex-item :first-of-type {
  text-transform: uppercase;
  color: rgb(144, 144, 144);
  /* font-size: 1.2rem; */
}

.flex-item :last-of-type {
  text-transform: uppercase;
  color: rgb(128, 128, 128);
  font-size: 1.2rem;
}
</style>
