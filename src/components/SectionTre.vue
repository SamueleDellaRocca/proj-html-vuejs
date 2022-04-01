<template>
  <div>
    <div class="sfondo">
      <div class="container">
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

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
  padding-bottom: 100px;
  .sinistra {
    width: 456px;
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
  }
}

.sfondo-2 {
  height: 132px;
  background-image: url(../assets/img/latestnews-bottom.png);
  background-size: cover;
  background-position: center;
  filter: invert(5%);
}
</style>
