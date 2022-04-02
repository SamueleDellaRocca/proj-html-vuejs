<template>
  <div>
    <div class="container mb">
      <h1 class="titolo">Your Instructors</h1>
      <div class="flex">
        <div class="testo">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Est, quasi
          blanditiis aut delectus nesciunt nisi totam sit ipsa nobis ipsam rem
          unde natus fugit officia quis rerum ullam accusantium obcaecati!
        </div>
        <div><button class="btn-nav">more about us</button></div>
      </div>
    </div>

    <div class="container flex2">
      <div v-for="carta in arrayIstruttori" :key="carta.nome" class="box">
        <div class="img">
          <img :src="require('../assets/img/' + carta.img)" :alt="carta.nome" />
        </div>
        <h1>{{ carta.nome }}</h1>
        <div class="logos">face twitt ista</div>
        <div class="text">
          Lorem ipsum dolor sit amet, consectetur adipipiscing elit.
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionQuattro",
  data() {
    return {
      arrayIstruttori: [
        {
          img: "instructor-mikehart.jpg",
          nome: "Mike Hart",
        },
        {
          img: "instructor-johnsmith.jpg",
          nome: "John Smith",
        },
        {
          img: "instructor-angelahart.jpg",
          nome: "Angela Hart",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.titolo {
  margin-bottom: 3rem;
}

.flex {
  display: flex;
  gap: 3rem;
}

.btn-nav {
  width: 350px;
  background-color: hsl(105deg 40% 56%);
  border-radius: 80px;
  color: white;
  text-transform: uppercase;
  font-weight: bold;
  padding: 13px 30px;
  border: 1px solid transparent;
  cursor: pointer;
}

.testo {
  line-height: 2rem;
}

.mb {
  margin-bottom: 5rem;
}

.flex2 {
  display: flex;
  gap: 1rem;
}

.box {
  width: 412px;
  height: 450px;
  background-color: white;
  text-align: center;
  padding: 2rem 3rem;
  border-radius: 15px;
  color: gray;
  box-shadow: 0px 30px 20px gray;
  border-top: 8px solid hsl(105deg 40% 56%);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .img {
    width: 100%;
    margin-bottom: 1rem;
    img {
      width: 100%;
    }
  }

  h1 {
    margin-bottom: 0.6rem;
  }
  .logos {
    margin-bottom: 0.5rem;
  }
}

.box:nth-child(2) {
  height: 470px;
  padding-bottom: 56px;
}
</style>
