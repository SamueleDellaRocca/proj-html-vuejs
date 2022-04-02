<template>
  <div class="sfondo">
    <div
      v-show="index == indexAttivo"
      v-for="(testimone, index) in arrayTestimoni"
      :key="testimone.nome"
      class="container"
    >
      <h1>Testimonials</h1>
      <div class="sottotitolo">
        Here's what our happy drivers had to say about our services:
      </div>

      <div class="img">
        <img
          :src="require('../assets/img/' + testimone.foto)"
          :alt="testimone.nome"
        />
      </div>
      <div class="testo">
        Avada Driving School really helped build my confidence behind the wheel
        and with driving in general, and they got me a first time pass!
      </div>
      <div class="sub-testo">Highly recommended.</div>
      <h4>{{ testimone.nome }}</h4>
      <div class="flex">
        <div
          @click="funzionePallino(index)"
          :class="{ 'pallino-pieno': index == indexAttivo }"
          v-for="(pallino, index) in arrayPallini"
          :key="pallino"
          class="pallino"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionCinque",
  data() {
    return {
      indexAttivo: 0,
      arrayPallini: ["a", "b", "c", "d", "e"],
      arrayTestimoni: [
        {
          foto: "testimonial-sophia.png",
          nome: "Sophia Jones",
        },
        {
          foto: "testimonial-grant.png",
          nome: "Grant Gary",
        },
        {
          foto: "testimonial-harold.png",
          nome: "Harold Smith",
        },
        {
          foto: "testimonial-kate.png",
          nome: "Kate Black",
        },
        {
          foto: "testimonial-kelly.png",
          nome: "Kelly Stones",
        },
      ],
    };
  },

  methods: {
    funzionePallino(index) {
      this.indexAttivo = index;
    },
  },
};
</script>

<style lang="scss" scoped>
.sfondo {
  height: 1050px;
  margin-top: -100px;
  background-image: url(../assets/img/testimonial-background.jpg);
  background-position: center;
  background-size: cover;
  display: flex;
}

.container {
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  align-items: center;
  color: gray;
  font-size: 1.5rem;
  padding: 13rem 10rem;

  .img {
    width: 180px;
    margin-bottom: 2rem;
    img {
      width: 100%;
    }
  }

  h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
    color: black;
  }

  .sottotitolo {
    margin-bottom: 4rem;
  }

  .testo {
    line-height: 2.5rem;
    font-size: 1.3rem;
    margin-bottom: 2rem;
  }

  .sub-testo {
    font-size: 1.3rem;
    margin-bottom: 3rem;
  }

  h4 {
    margin-bottom: 3rem;
  }

  .flex {
    display: flex;
    gap: 1rem;
  }

  .pallino {
    height: 16px;
    width: 16px;
    border-radius: 50%;
    border: 1px solid gray;
  }

  .pallino-pieno {
    background-color: gray;
  }
}
</style>
