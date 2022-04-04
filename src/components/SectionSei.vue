<template>
  <div class="sfondo">
    <div class="container">
      <div class="box">
        <h1>Latest News</h1>
        <div class="flex">
          <div class="carta">
            <div class="img">
              <img src="../assets/img/blog-choosecar-320x202.jpg" alt="" />
            </div>
            <h2>What Car to Start With?</h2>
            <div class="small">Febraury 7th 2019 | <span>0 comments</span></div>
            <div>Lorem ipsum dolor sit amet, consecteurs adipiscing</div>
          </div>

          <div class="carta">
            <div class="img">
              <img src="../assets/img/blogpost-10and2-320x202.jpg" alt="" />
            </div>
            <h2>What Car to Start With?</h2>
            <div class="small">Febraury 7th 2019 | <span>0 comments</span></div>
            <div>Lorem ipsum dolor sit amet, consecteurs adipiscing</div>
          </div>
        </div>
        <div><button class="btn-nav">more from the blog</button></div>
      </div>
      <div class="freccia"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionSei",
};
</script>

<style lang="scss" scoped>
.sfondo {
  height: 750px;
  background-image: url(../assets/img/latestnews-background.jpg);
  background-size: cover;
  background-position: center;
  display: flex;
}

.container {
  margin-top: -100px;
}

.box {
  width: 100%;
  height: 650px;
  background-color: white;
  text-align: center;
  padding: 2rem 3rem;
  border-radius: 15px;
  color: rgb(194, 193, 193);
  box-shadow: 0px 30px 20px gray;
  border-top: 8px solid hsl(202deg 25% 57%);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  h1 {
    font-size: 3rem;
    color: black;
    margin-bottom: 4rem;
  }

  .flex {
    display: flex;
    gap: 2rem;
    width: 100%;
    margin-bottom: 2rem;
    .carta {
      width: 50%;
      .img {
        width: 100%;
        img {
          width: 100%;
        }
      }

      h2 {
        color: hsl(105deg 40% 56%);
        margin-top: 1rem;
        margin-bottom: 8px;
      }

      .small {
        font-size: 0.9rem;
        margin-bottom: 1.3rem;
      }

      span {
        color: hsl(105deg 40% 56%);
      }
    }
  }
}

.btn-nav {
  width: 250px;
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

.freccia {
  width: 100%;
  height: 132px;
  background-image: url(../assets/img/latestnews-bottom.png);
  background-size: cover;
  background-position: center;
  margin-top: -33px;
}
</style>
