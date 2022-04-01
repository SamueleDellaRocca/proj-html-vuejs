<template>
  <div class="sfondo">
    <div class="container">
      <div class="sinistra">
        <h1>Start Learning to Drive Today</h1>
        <h3>Give us a call to schedule your first driving lesson</h3>
      </div>
      <div class="destra">1-800-555-555</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionDue",
};
</script>

<style lang="scss" scoped>
.sfondo {
  height: 230px;
  background-image: url(../assets/img/horizontal-cta-background.jpg);
  background-position: center;
  background-size: cover;
  .container {
    height: 100%;
    color: white;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .sinistra {
      h1 {
        font-size: 2.5rem;
      }
    }

    .destra {
      font-size: 2.5rem;
    }
  }
}
</style>
