<template>
  <div class="app">
    <div class="app-container">
      <FlexContainer :secondaryItemCount="4" />
      <FlexContainer :secondaryItemCount="6" />
      <FlexContainer :secondaryItemCount="5" />
      <FlexContainer :secondaryItemCount="3" />
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
  height: 100%;
  padding: 0;
  margin: 0;
  background-image: url("./assets/background.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

.app {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.app-container {
  max-width: 70%;
  padding: 3rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: rgba(255, 255, 255, 0.63);
  box-shadow: 5px 10px 18px #888888;
}

.app-container > div:not(:last-child) {
  margin-bottom: 1rem;
}
</style>
