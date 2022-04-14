<template>
  <div class="container">
    <div class="sinistra">
      <h3>Get Behind The Wheel</h3>
      <div>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem rem
        molestiae perferendis mea amet?m ipsum dolor sit, amet consectetur
        adipisicing elit. Iure omnis et modi veniam nihil? Est eaque ut sed
        tempore laudantium pe
      </div>
      <small
        >Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iure omnis et
        modi veniam nihil? Est eaque ut sed tempore laudantium perferendis,
        suscipit distinctio itaque aperiam inventore iusto minima incidunt m
        ipsum dolor sit, amet consectetur adipisicing elit. Iure omnis et modi
        veniam nihil? Est eaque ut sed tempore laudantium perferendis, suscipit
        distinctio itaque aperiam inventore iusto minima incidunt dicta.</small
      >
    </div>
    <div class="destra">
      <h4>First Lesson Free!</h4>
      <div class="text">
        When you make a block booking with us your first lesson is included
        free.
      </div>

      <div class="form">
        <form action="">
          <input
            v-for="input in arrayInput"
            :key="input.name"
            :type="input.type"
            :name="input.name"
            :id="input.id"
            :placeholder="input.placeholder"
            class="input"
          />
        </form>
        <div class="adesivo"><img src="../assets/img/image.png" alt="" /></div>
      </div>

      <!-- <div><button class="btn-nav">request a callback</button></div> -->
      <botton-driving :text="text"></botton-driving>
    </div>
  </div>
</template>

<script>
import BottonDriving from "./BottonDriving.vue";
export default {
  name: "SectionUno",

  components: {
    BottonDriving,
  },

  data() {
    return {
      text: "request a callback",

      arrayInput: [
        {
          type: "text",
          name: "name",
          id: "name",
          placeholder: "Your Name*",
        },
        {
          type: "email",
          name: "email",
          id: "email",
          placeholder: "Email*",
        },
        {
          type: "tel",
          name: "tel",
          id: "tel",
          placeholder: "Telephone",
        },
        {
          type: "text",
          name: "location",
          id: "location",
          placeholder: "Location",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  height: 350px;
  justify-content: space-evenly;
  align-items: center;
  margin-bottom: 150px;

  .sinistra {
    width: 55%;
    height: 100%;
    align-self: center;
    padding-right: 70px;
    margin-top: 70px;
    h3 {
      font-size: 2rem;
      margin-bottom: 30px;
    }
    div {
      line-height: 35px;
      margin-bottom: 20px;
      color: gray;
      font-size: 1.2rem;
    }
    small {
      color: gray;
      font-size: 1rem;
    }
  }

  .destra {
    width: 45%;
    height: 500px;
    background-color: white;
    text-align: center;
    padding: 2rem 3rem;
    border-radius: 15px;
    color: gray;
    box-shadow: 0px 30px 20px gray;
    z-index: 2;

    h4 {
      color: hsl(105deg 40% 56%);
      font-size: 2rem;
      margin-bottom: 1.5rem;
    }

    .text {
      margin-bottom: 1rem;
    }

    .form {
      input {
        width: 100%;
        height: 3rem;
        margin-bottom: 1.1rem;
        border-radius: 5px;
        padding: 0px 10px;
        background-color: rgb(201, 201, 201, 0.2);
      }

      .input:first-child {
        position: relative;
      }

      .adesivo {
        position: absolute;
        right: 16%;
        bottom: -13%;
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
</style>
