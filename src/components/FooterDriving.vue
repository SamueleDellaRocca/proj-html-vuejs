<template>
  <div id="footer">
    <div class="sfondo">
      <div class="container flexato">
        <div class="numero1">
          <div class="img">
            <img src="../assets/img/avada-drivers-logo-1x.png" alt="ft-logo" />
          </div>
          <div>
            Avada Driving School is the right choice for experienced drivers
            looking for a refresher course, or the brand new driver wanting to
            pass firts time.
          </div>
        </div>
        <div class="numero2">
          <h3>CONTACT DETAILS</h3>
          <ul class="ul">
            <li>
              <a href="#footer"
                ><font-awesome-icon
                  icon="fa-solid fa-house-chimney"
                  class="icon"
              /></a>
              <a href="#footer"
                >12345 North Main Street, New York, NY 5555555</a
              >
            </li>
            <li>
              <a href="#footer">
                <font-awesome-icon
                  icon="fa-solid fa-phone-flip"
                  class="icon"
                />1.800.555.6789</a
              >
            </li>
            <li>
              <a href="#footer"
                ><font-awesome-icon
                  icon="fa-solid fa-envelope"
                  class="icon"
                />info@your-domain.com</a
              >
            </li>
            <li>
              <a href="#footer"
                ><font-awesome-icon
                  icon="fa-solid fa-link"
                  class="icon"
                />Theme-Fusion.com</a
              >
            </li>
          </ul>
        </div>
        <div class="numero2">
          <h3>COURSES</h3>
          <ul class="lista">
            <li>
              <a class="green" href="#footer"
                ><font-awesome-icon
                  icon="fa-solid fa-circle-arrow-right"
                  class="icon"
                />Pass Plus</a
              >
            </li>
            <li>
              <a class="green" href="#footer"
                ><font-awesome-icon
                  icon="fa-solid fa-circle-arrow-right"
                  class="icon"
                />Intensive Course</a
              >
            </li>
            <li>
              <a class="green" href="#footer"
                ><font-awesome-icon
                  icon="fa-solid fa-circle-arrow-right"
                  class="icon"
                />Automatic</a
              >
            </li>
            <li>
              <a class="green" href="#footer"
                ><font-awesome-icon
                  icon="fa-solid fa-circle-arrow-right"
                  class="icon"
                />Instructor Training</a
              >
            </li>
          </ul>
        </div>
        <div class="numero4">
          <div class="img">
            <img src="../assets/img/footer-ad-grid.png" alt="ft-grid" />
          </div>
          <div>
            <!-- <button class="btn-nav">Book Now</button> -->
            <botton-driving :text="text"></botton-driving>
          </div>
        </div>
      </div>
    </div>

    <div class="sfondo2">
      <div class="container crediti">
        <div>
          @ Copyright 2012-2020 | Avada Theme by <span>ThemeFusion</span> | All
          rights reserved | Powered by <span>WordPress</span>
        </div>
        <div class="ic-flex">
          <font-awesome-icon icon="fa-brands fa-facebook-f" />
          <font-awesome-icon icon="fa-brands fa-twitter" />
          <font-awesome-icon icon="fa-brands fa-youtube" />
          <font-awesome-icon icon="fa-brands fa-instagram" />
        </div>
      </div>
      <div class="freccia">
        <a href="#header"><font-awesome-icon icon="fa-solid fa-angle-up" /></a>
      </div>
    </div>
  </div>
</template>

<script>
import BottonDriving from "./BottonDriving.vue";
export default {
  components: { BottonDriving },
  name: "FooterDriving",

  data() {
    return {
      text: "book now",
    };
  },
};
</script>

<style lang="scss" scoped>
.ul li {
  display: flex;
}

.icon {
  margin-right: 1rem;
}

.sfondo {
  height: 450px;
  background-image: url(../assets/img/footer-background-color.jpg);
  background-size: cover;
  background-position: center;

  .flexato {
    height: 100%;
    display: flex;
    gap: 4rem;
    line-height: 1.5rem;
    padding: 5rem 0px;

    .numero1 {
      width: 25%;
      color: gray;
      font-size: 0.9rem;
      .img {
        width: 90%;
        img {
          width: 100%;
        }
      }
    }

    .numero2 {
      width: 18%;
      h3 {
        color: white;
        margin-bottom: 1rem;
      }

      ul {
        list-style: none;

        li {
          padding: 0.6rem 0px;
          a {
            text-decoration: none;
            color: gray;
            font-size: 0.9rem;
          }
        }
      }
    }

    .lista {
      li {
        .green {
          font-size: 1.2rem;
          color: hsl(105deg 29% 51%);
        }
      }
    }

    .numero4 {
      width: 23%;
      display: flex;
      flex-direction: column;
      align-items: center;
      .img {
        width: 100%;
        img {
          width: 100%;
          margin-bottom: 10px;
        }
      }
      // .btn-nav {
      //   background-color: hsl(105deg 40% 56%);
      //   border-radius: 80px;
      //   color: white;
      //   text-transform: uppercase;
      //   font-weight: bold;
      //   padding: 13px 30px;
      //   border: 1px solid transparent;
      //   cursor: pointer;
      // }

      // .btn-nav:hover {
      //   transition: 0.4s;
      //   box-shadow: 0px 0px 20px hsl(105deg 40% 56%);
      // }
    }
  }
}

.sfondo2 {
  height: 130px;
  background-color: hsl(210deg 3% 11%);
  position: relative;

  .freccia {
    position: absolute;
    bottom: 5px;
    right: 100px;
    a {
      color: white;
      text-decoration: none;
      background-color: gray;
      padding: 5px 16px;
    }
  }
}

.ic-flex {
  display: flex;
  color: white;
  font-size: 1rem;
  gap: 1.1rem;
}

.crediti {
  color: gray;
  height: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.9rem;

  span {
    color: hsl(105deg 40% 56%);
  }
}
</style>
