<template>
  <div>
    <SectionUno />
    <SectionDue />
    <section-tre />
    <section-quattro />
    <section-cinque />
    <section-sei />
    <section-sette />
  </div>
</template>

<script>
import SectionDue from "./SectionDue.vue";
import SectionTre from "./SectionTre.vue";
import SectionUno from "./SectionUno.vue";
import SectionQuattro from "./SectionQuattro.vue";
import SectionCinque from "./SectionCinque.vue";
import SectionSei from "./SectionSei.vue";
import SectionSette from "./SectionSette.vue";

export default {
  name: "MainDriving",
  components: {
    SectionUno,
    SectionDue,
    SectionTre,
    SectionQuattro,
    SectionCinque,
    SectionSei,
    SectionSette,
  },
};
</script>

<style lang="scss" scoped></style>
