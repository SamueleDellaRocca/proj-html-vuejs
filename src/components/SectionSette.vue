<template>
  <div class="sfondo">
    <div class="container">
      <h1>Sign up to our Newsletter</h1>
      <input type="email" name="email" id="email" />
      <!-- <div><button class="btn-nav">subscribe</button></div> -->
      <botton-driving class="btn-prova" :text="text"></botton-driving>
      <small>
        (We do not share your data with anybody, and only use it for its inteded
        purpose)
      </small>
    </div>
  </div>
</template>

<script>
import BottonDriving from "./BottonDriving.vue";
export default {
  components: { BottonDriving },
  name: "SectionSette",

  data() {
    return {
      text: "subscribe",
    };
  },
};
</script>

<style lang="scss" scoped>
.sfondo {
  height: 400px;
  background-image: url(../assets/img/newsletter_background.jpg);
  background-size: cover;
  background-position: center;
}

h1 {
  color: hsl(206deg 5% 30%);
  margin-bottom: 1.2rem;
}

input {
  width: 600px;
  line-height: 3rem;
  font-size: 1.6rem;
  border-radius: 5px;
  border: 1px solid lightgray;
}

.container {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 2rem;
}

.btn-prova {
  width: 580px;
  // background-color: hsl(105deg 40% 56%);
  // border-radius: 80px;
  // color: white;
  // text-transform: uppercase;
  // font-weight: bold;
  // padding: 13px 30px;
  // border: 1px solid transparent;
  // cursor: pointer;
}

.btn-nav:hover {
  transition: 0.4s;
  box-shadow: 0px 0px 20px hsl(105deg 40% 56%);
}

small {
  color: gray;
}
</style>
