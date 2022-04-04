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
          <div class="effetto-hover">{{ carta.instructor }}</div>
        </div>
        <h1>{{ carta.nome }}</h1>
        <div class="logos">
          <font-awesome-icon icon="fa-brands fa-facebook-f" />
          <font-awesome-icon icon="fa-brands fa-twitter" />
          <font-awesome-icon icon="fa-brands fa-instagram" />
        </div>
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
          instructor: "instructor-mikehart",
        },
        {
          img: "instructor-johnsmith.jpg",
          nome: "John Smith",
          instructor: "instructor-johnsmith",
        },
        {
          img: "instructor-angelahart.jpg",
          nome: "Angela Hart",
          instructor: "instructor-angelahart",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.logos {
  display: flex;
  gap: 1rem;
  margin: 10px 0px;
}

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

.btn-nav:hover {
  transition: 0.4s;
  box-shadow: 0px 0px 20px hsl(105deg 40% 56%);
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
  width: 33%;
  height: 450px;
  background-color: white;
  text-align: center;
  padding: 2rem 3rem;
  border-radius: 15px;
  color: darkgray;
  box-shadow: 0px 30px 20px gray;
  border-top: 8px solid hsl(105deg 40% 56%);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .img {
    width: 100%;
    margin-bottom: 1rem;
    position: relative;
    img {
      width: 100%;
    }
    .effetto-hover {
      border: 1px solid black;
      background-color: white;
      position: absolute;
      right: 2px;
      bottom: 30px;
      cursor: pointer;
      padding: 3px 6px;
      color: black;
      font-size: 0.8rem;
      visibility: hidden;
    }
  }

  .img:hover .effetto-hover {
    visibility: visible;
  }

  h1 {
    color: gray;
    margin-bottom: 0.6rem;
  }

  .text {
    line-height: 2rem;
  }
}

.box:nth-child(2) {
  height: 470px;
  padding-bottom: 56px;
}
</style>
