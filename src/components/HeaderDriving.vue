<template>
  <header id="header">
    <div class="bg">
      <div class="container barra-superiore">
        <div>We have a 95% Successful Pass Rate!</div>
        <div>
          <font-awesome-icon icon="fa-solid fa-phone-flip" class="phone" />Give
          us a call to book your tuition! 1-800-555-555
        </div>
      </div>
    </div>

    <div class="sfondo-header">
      <div class="sfondo-nav">
        <nav class="container">
          <div class="mr">
            <img src="../assets/img/avada-drivers-logo-1x.png" alt="" />
          </div>

          <div style="width: 60%">
            <ul class="lista">
              <li v-for="elemento in arrayNav" :key="elemento.text">
                <a href="">{{ elemento.text }} </a>
              </li>
            </ul>
          </div>
          <div class="new"><button>NEW</button></div>

          <!-- <div><button class="btn-nav">Book Now</button></div> -->
          <botton-driving :text="text"></botton-driving>
        </nav>
      </div>

      <div class="container titolo">
        <h1>Drive with Avada</h1>
        <h2>We offer the finest driving tuition money can buy</h2>

        <div class="boxes">
          <div class="box">
            <div>
              <font-awesome-icon
                icon="fa-solid fa-folder-plus"
                class="folder"
              />
            </div>
            <small>Demos</small>
          </div>
          <div class="box verde">
            <h3>$39</h3>
            <small>On Sale</small>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import BottonDriving from "./BottonDriving";
export default {
  name: "HeaderDriving",

  components: {
    BottonDriving,
  },

  data() {
    return {
      text: "Book Now",

      arrayNav: [
        {
          text: "Home",
        },
        {
          text: "About",
        },
        {
          text: "Prices",
        },
        {
          text: "Courses",
        },
        {
          text: "Location",
        },
        {
          text: "Blog",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.boxes {
  display: flex;
  flex-direction: column;
  gap: 10px;
  position: absolute;
  right: 2%;
  top: 13%;
}

.box {
  height: 60px;
  width: 60px;
  border-radius: 5px;
  color: black;
  background-color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  .folder {
    font-size: 2rem;
  }
}
.verde {
  color: hsl(105deg 40% 56%);
  small {
    color: black;
  }
}

.bg {
  background-color: hsl(210deg 2% 21%);
  color: gray;
}

.barra-superiore {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 50px;
  font-size: 0.8rem;
}

.phone {
  margin-right: 10px;
}

.sfondo-header {
  height: 650px;
  width: 100%;
  background-image: url(../assets/img/homepage-hero-background.jpg);
  background-size: cover;
  background-position: center;
  position: relative;
}

.sfondo-nav {
  min-height: 110px;
  background-color: rgba(32, 32, 32, 0.5);
  display: flex;
  align-content: center;
}

nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  height: 100%;
}

.mr {
  margin-right: 40px;
}

.lista {
  list-style: none;
  display: flex;
  width: 100%;
  justify-content: space-between;
  position: relative;
  li {
    a {
      text-decoration: none;
      color: white;
      text-transform: uppercase;
      font-weight: bold;
      padding-bottom: 10px;
      border-bottom: 4px solid transparent;
    }
  }
}

li a:hover {
  color: hsl(105deg 40% 56%);
  border-bottom: 4px solid hsl(105deg 40% 56%);
}

// .btn-test {
// background-color: hsl(105deg 40% 56%);
//   border-radius: 80px;
//   color: white;
//   text-transform: uppercase;
//   font-weight: bold;
// padding: 80px 30px;
//   border: 1px solid transparent;
//   cursor: pointer;
// }

.btn-nav:hover {
  transition: 0.4s;
  box-shadow: 0px 0px 20px hsl(105deg 40% 56%);
}

.new {
  position: absolute;
  right: 36.5%;

  button {
    background-color: hsl(105deg 40% 56%);
    color: white;
    text-transform: uppercase;
    font-weight: bold;
    font-size: 0.7rem;
    border: 1px solid transparent;
    padding: 2px 3px;
    border-radius: 5px;
    cursor: pointer;
  }
}

.titolo {
  color: white;
  margin-top: 177px;
  h1 {
    font-size: 4rem;
  }
  h2 {
    font-size: 1.8rem;
  }
}
</style>
