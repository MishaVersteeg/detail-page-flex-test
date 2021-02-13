<template>
  <div class="container">
    <div class="header">Aggregated risks</div>
    <div class="body">
      <div class="col-1">
        <div class="chart" />
      </div>
      <div class="col-2">
        <div v-for="i in 2" :key="i">
          <TotalContainer />
        </div>
      </div>
      <div class="col-3">
        <div v-for="i in secondaryItemCount" :key="i">
          <TotalContainer />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TotalContainer from "./TotalContainer";

export default {
  props: {
    secondaryItemCount: Number,
  },

  components: {
    TotalContainer,
  },
};
</script>

<style scoped>
.container {
  width: 120rem;
  max-width: 90%;
  padding: 1rem calc(1rem - 0.2rem) calc(1rem - 0.2rem) 1rem;
  background: rgb(245, 242, 240);
  border-radius: 7px;
  box-shadow: 5px 10px 10px #b6b6b6;
}

.header {
  padding: 0 0 1rem;
}

.body {
  display: flex;
}

.col-1 {
  display: flex;
  align-items: center;
  margin-right: 0.2rem;
  border-bottom: 0.2rem solid rgba(245, 242, 240, 0);
}

.col-1 > div {
  height: 100%;
  max-height: 10rem;
  width: 0.7rem;

  background: linear-gradient(rgb(255, 136, 0), rgb(251, 255, 0));
}

.col-2 {
  display: flex;
  flex-wrap: wrap;
  flex: 0 1 35%;
}

.col-2 > div {
  flex: 1;
  min-width: 6rem;
  background: rgb(206, 224, 223);
}

.col-3 {
  flex: 1;
  display: flex;
  flex-wrap: wrap;
}

.col-3 > div {
  background: rgb(240, 221, 206);
}

@media only screen and (min-width: 1500px) {
  .col-3 > div {
    flex: 0 1 25%;
  }
}

@media only screen and (max-width: 1500px) {
  .col-3 > div {
    flex: 0 1 50%;
  }
}

@media only screen and (max-width: 800px) {
  .col-3 > div {
    flex: 0 1 100%;
  }
}
</style>
