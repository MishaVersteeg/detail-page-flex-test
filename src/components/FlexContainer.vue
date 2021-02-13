<template>
  <div class="container">
    <div class="col-1">
      <div class="chart" />
    </div>
    <div class="col-2">
      <div>
        <FlexItem />
      </div>
      <div>
        <FlexItem />
      </div>
    </div>
    <div class="col-3">
      <div v-for="i in secondaryItemCount" :key="i">
        <FlexItem />
      </div>
    </div>
  </div>
</template>

<script>
import FlexItem from "./FlexItem";

export default {
  props: {
    secondaryItemCount: Number,
  },

  components: {
    FlexItem,
  },
};
</script>

<style scoped>
.container {
  width: 60rem;
  max-width: 90%;
  padding: 0.5rem calc(0.5rem - 0.1rem) calc(0.5rem - 0.1rem) 0.5rem;

  background: rgb(233, 217, 217);
  box-shadow: 5px 10px 18px #888888;

  display: flex;
}

.col-1 {
  display: flex;
  align-items: center;
}
.col-1 > div {
  height: 100%;
  max-height: 6rem;
  width: 0.7rem;
  margin-right: 0.1rem;
  background: linear-gradient(rgb(255, 0, 0), rgb(251, 255, 0));
}

.col-2 {
  display: flex;
  flex: 0 1 35%;
}

.col-2 > div {
  flex: 1;
  background: rgb(206, 171, 146);
}

.col-3 {
  flex: 1;
  display: flex;
  flex-wrap: wrap;
}

.col-3 > div {
  flex: 0 1 25%;
  background: rgb(226, 199, 179);
}
</style>
