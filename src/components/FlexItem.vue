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
    randomNumber: () => Math.floor(Math.random() * 1000),

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

  padding:  1rem 0.5rem;

  box-sizing: border-box;
  border-right: 0.1rem solid rgb(233, 217, 217);
  border-bottom: 0.1rem solid rgb(233, 217, 217);
}
</style>
