<template>
  <div>
    <div class="sfondo">
      <div class="container flexato">
        <div class="sinistra">
          <div class="corner">
            <img src="../assets/img/new-corner.jpg" alt="new-corner" />
          </div>

          <h4>Courses</h4>
          <div class="text">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Veniam rem
            quod rerum vero maxime officiis similique temporibus necessitatibus
            consequuntur aut quae nihil obcaecati, magni vel nisi! Atque nemo
            reiciendis dolorem?
          </div>
          <div><button class="btn-nav">course information</button></div>
        </div>

        <div class="destra">
          <div v-for="carta in arrayCourses" :key="carta.img" class="carta">
            <div class="foto">
              <img
                :src="require('../assets/img/' + carta.img)"
                :alt="carta.titolo"
              />
            </div>
            <h3>{{ carta.titolo }}</h3>
            <div><button class="btn-more">learn more</button></div>
          </div>
        </div>
      </div>
    </div>
    <div class="sfondo-2"></div>
    <div class="container flex">
      <!-- commento il ciclo per fare l effetto -->
      <!-- <div v-for="carta in arrayCerchi" :key="carta.percentuale" class="box">
        <div class="cerchio">{{ carta.percentuale }}</div>
        <h3>{{ carta.titolo }}</h3>
      </div> -->

      <div class="box">
        <div class="percent">
          <svg>
            <circle cx="70" cy="70" r="70"></circle>
            <circle cx="70" cy="70" r="70"></circle>
          </svg>
        </div>

        <div class="number"><h2>87%</h2></div>
        <h3>PASS RATE</h3>
      </div>

      <div class="box">
        <div class="percent">
          <svg>
            <circle cx="70" cy="70" r="70"></circle>
            <circle cx="70" cy="70" r="70"></circle>
          </svg>
        </div>

        <div class="number"><h2>100%</h2></div>
        <h3>REFERRAL RATE</h3>
      </div>

      <div class="box">
        <div class="percent">
          <svg>
            <circle cx="70" cy="70" r="70"></circle>
            <circle cx="70" cy="70" r="70"></circle>
          </svg>
        </div>

        <div class="number"><h2>0%</h2></div>
        <h3>ACCIDENT RATE</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionTre",
  data() {
    return {
      arrayCourses: [
        {
          img: "courses-passplus.jpg",
          titolo: "Pass Plus",
        },
        {
          img: "course-intensive.jpg",
          titolo: "Intensive Course",
        },
        {
          img: "courses-instructor.jpg",
          titolo: "Instructors",
        },
      ],

      arrayCerchi: [
        {
          percentuale: "95%",
          titolo: "PASS RATE",
        },
        {
          percentuale: "100%",
          titolo: "REFERRAL RATE",
        },
        {
          percentuale: "0%",
          titolo: "ACCIDENT RATE",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.sfondo {
  height: 400px;
  background-image: url(../assets/img/promise-background.jpg);
  background-size: cover;
  background-position: center;
}

.flexato {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
  padding-bottom: 100px;
  .sinistra {
    min-width: 412px;
    height: 350px;
    background-color: white;
    text-align: center;
    padding: 2rem 3rem;
    border-radius: 15px;
    color: gray;
    box-shadow: 0px 30px 20px gray;
    overflow: hidden;
    position: relative;

    .corner {
      position: absolute;
      left: 0px;
      top: 0px;
      width: 90px;
      img {
        width: 100%;
      }
    }

    h4 {
      color: black;
      font-size: 2rem;
      margin-bottom: 1.5rem;
    }

    .text {
      margin-bottom: 2rem;
    }

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
  }

  .destra {
    padding-top: 4rem;
    color: hsl(205deg 32% 62%);
    display: flex;
    .carta {
      width: 180px;
      margin: 2rem;
      text-align: center;
    }
    img {
      width: 100%;
    }
    .foto {
      margin-bottom: 1rem;
    }

    .btn-more {
      color: hsl(205deg 32% 62%);
      border-radius: 80px;
      text-transform: uppercase;
      font-weight: bold;
      padding: 8px 30px;
      border: 3px solid hsl(205deg 32% 62%);
      cursor: pointer;
      margin-top: 10px;
    }

    .btn-more:hover {
      border: 3px solid hsl(105deg 40% 56%);
      color: hsl(105deg 40% 56%);
    }
  }
}

.sfondo-2 {
  height: 132px;
  background-image: url(../assets/img/latestnews-bottom.png);
  background-size: cover;
  background-position: center;
  filter: invert(5%);
  margin-bottom: -100px;
  z-index: -1;
  position: relative;
}

.flex {
  display: flex;
  gap: 1rem;
  height: 415px;
  padding-bottom: 100px;
  z-index: 10;
  margin-bottom: 12rem;
}
.box {
  width: 412px;
  height: 430px;
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
  position: relative;

  h3 {
    text-transform: uppercase;
  }

  .percent {
    position: relative;
    width: 150px;
    height: 150px;
    margin: 2rem;
  }

  .percent svg circle:nth-child(1) {
    stroke-dashoffset: 0;
    stroke: #f3f3f3;
  }

  .percent svg circle:nth-child(2) {
    stroke-dashoffset: calc(440 - (440 * 87) / 100);
    stroke: hsl(105deg 40% 56%);
  }

  svg {
    position: relative;
    width: 150px;
    height: 150px;
  }

  circle {
    width: 150px;
    height: 150px;
    fill: none;
    stroke-width: 10;
    stroke: hsl(105deg 40% 56%);
    transform: translate(5px, 5px);
    stroke-dasharray: 440;
    stroke-dashoffset: 440;
    stroke-linecap: round;
  }

  .number {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    h2 {
      font-size: 3rem;
    }
  }

  h3 {
    position: absolute;
    top: 320px;
  }
}

.box:nth-child(2) {
  .percent svg circle:nth-child(2) {
    stroke-dashoffset: calc(440 - (440 * 100) / 100);
    stroke: hsl(105deg 40% 56%);
  }
}

.box:nth-child(3) {
  .percent svg circle:nth-child(2) {
    stroke-dashoffset: calc(440 - (440 * 1) / 100);
    stroke: hsl(105deg 40% 56%);
  }
}
</style>
