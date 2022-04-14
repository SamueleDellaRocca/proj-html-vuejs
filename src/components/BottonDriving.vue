<template>
  <button class="btn-nav">{{ text }}</button>
</template>

<script>
export default {
  name: "BottonDriving",

  props: {
    text: String,
  },
};
</script>

<style lang="scss" scoped>
.btn-nav {
  background-color: hsl(105deg 40% 56%);
  border-radius: 80px;
  color: white;
  text-transform: uppercase;
  font-weight: bold;
  padding: 13px 30px;
  border: 1px solid transparent;
  cursor: pointer;
}

.btn-nav:hover {
  transition: 0.4s;
  box-shadow: 0px 0px 20px hsl(105deg 40% 56%);
}
</style>
