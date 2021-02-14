<template>
  <div class="app">
    <div class="app-container">
      <FlexContainer :secondaryItemCount="4" />
      <FlexContainer :secondaryItemCount="6" />
      <FlexContainer :secondaryItemCount="5" />
      <FlexContainer :secondaryItemCount="7" />
    </div>
  </div>
</template>

<script>
import FlexContainer from "@/components/FlexContainer";

export default {
  components: {
    FlexContainer,
  },
};
</script>

<style>
body,
html {
  min-height: 100vh;
  padding: 0;
  margin: 0;
  background-image: url("./assets/background.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

/* experimental: */
* {
  /* transition: all 1s ease-in-out; */
}

.app {
  display: flex;
  justify-content: center;
  align-items: center;
}

.app-container {
  max-width: 70%;
  margin: 3rem 0;
  padding: 3rem;
  background: rgba(156, 204, 207, 0.294);
  border-radius: 20px;
  box-shadow: 5px 10px 30px #888888;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.app-container > div:not(:last-child) {
  margin-bottom: 1rem;
}

.border {
  border: 1px solid pink;
}
</style>
