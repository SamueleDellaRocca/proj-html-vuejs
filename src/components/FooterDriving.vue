<template>
  <div>
    <div class="sfondo">
      <div class="container"></div>
    </div>

    <div class="sfondo2">
      <div class="container crediti">
        <div>
          @ Copyright 2012-2020 | Avada Theme by <span>ThemeFusion</span> | All
          rights reserved | Powered by <span>WordPress</span>
        </div>
        <div>face twit yout ista</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterDriving",
};
</script>

<style lang="scss" scoped>
.sfondo {
  height: 450px;
  background-image: url(../assets/img/footer-background-color.jpg);
  background-size: cover;
  background-position: center;
}

.sfondo2 {
  height: 130px;
  background-color: hsl(210deg 3% 11%);
}

.crediti {
  color: gray;
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.9rem;

  span {
    color: hsl(105deg 40% 56%);
  }
}
</style>
