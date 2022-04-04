<template>
  <header id="header">
    <div class="bg">
      <div class="container barra-superiore">
        <div>We have a 95% Successful Pass Rate!</div>
        <div>Give us a call to book your tuition! 1-800-555-555</div>
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

          <div><button class="btn-nav">Book Now</button></div>
        </nav>
      </div>

      <div class="container titolo">
        <h1>Drive with Avada</h1>
        <h2>We offer the finest driving tuition money can buy</h2>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderDriving",

  data() {
    return {
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

.sfondo-header {
  height: 650px;
  width: 100%;
  background-image: url(../assets/img/homepage-hero-background.jpg);
  background-size: cover;
  background-position: center;
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
