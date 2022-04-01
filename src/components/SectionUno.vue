<template>
  <div class="container">
    <div class="sinistra">
      <h3>Get Behind The Wheel</h3>
      <div>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem rem
        molestiae perferendis mea amet?m ipsum dolor sit, amet consectetur
        adipisicing elit. Iure omnis et modi veniam nihil? Est eaque ut sed
        tempore laudantium pe
      </div>
      <small
        >Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iure omnis et
        modi veniam nihil? Est eaque ut sed tempore laudantium perferendis,
        suscipit distinctio itaque aperiam inventore iusto minima incidunt m
        ipsum dolor sit, amet consectetur adipisicing elit. Iure omnis et modi
        veniam nihil? Est eaque ut sed tempore laudantium perferendis, suscipit
        distinctio itaque aperiam inventore iusto minima incidunt dicta.</small
      >
    </div>
    <div class="destra"></div>
  </div>
</template>

<script>
export default {
  name: "SectionUno",
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  height: 350px;
  justify-content: space-evenly;
  align-items: center;
  margin-bottom: 150px;

  .sinistra {
    width: 50%;
    height: 100%;
    align-self: center;
    padding-right: 30px;
    margin-top: 70px;
    h3 {
      font-size: 2rem;
      margin-bottom: 30px;
    }
    div {
      line-height: 35px;
      margin-bottom: 20px;
      color: gray;
    }
    small {
      color: gray;
    }
  }

  .destra {
    width: 50%;
    height: 500px;
    background-color: lightgreen;
  }
}
</style>
