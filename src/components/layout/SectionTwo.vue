<template>
  <div class="section s2" data-scroll-section>
    <div class="cl1" data-scroll data-scroll-speed="2">
      <div class="s2-img s2_1">
        <div
          class="s2-imginner"
        ></div>
      </div>
      <div class="cl1-txt">
        <div class="header">Join to our models</div>
        <p>
          We are currently looking for new faces. Discover our women and join us
          as soon as possible.
        </p>
      </div>
    </div>
    <div class="cl2">
      <div class="cl2-txt">
        <div class="header">How to become a model</div>
        <p>
          if you are a woman, and you are not over 21 years old: you have to be
          at least 1,74 cms tall, your waist max 60 cms and hip size not over 90
          cms (these measurements have to be by nature and not the result of an
          unhealthy diet!).
        </p>
      </div>
      <div class="s2-img s2_2">
        <div
          class="cl2-imginner"
        ></div>
      </div>
    </div>
    <div class="cl3" data-scroll data-scroll-speed="3">
      <div class="s2-img s2_3">
        <div
          class="cl3-imginner"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionTwo",
};
</script>

<style scoped>
.s2 {
  grid-area: s2;
  display: grid;
  grid-template-areas: "cl1 cl2";
  grid-template-columns: 50% 50%;
  justify-content: center;
}
.s2 .cl1 {
  grid-area: cl2;
  padding: 17rem 1rem 0 1rem;
}
.s2 .cl2 {
  grid-area: cl1;
}

.s2 .cl3 {
  grid-area: cl2;
  padding: 17rem 0 0 0;
}

.s2-img {
  overflow: hidden;
}
.s2_1 .s2-imginner {
    background: url("../../assets/img/s2_1.jpg");
  background-size: auto 105%;
  background-position: -30% 0%;
  background-repeat: no-repeat;
  padding: 82%;
}
.s2 .cl1 .cl1-txt .header {
  font-size: 1.3rem;
  margin: 4rem 0 0;
  padding: 0;
  color: var(--color-header);
}
.s2 .cl2 .cl2-txt .header {
  font-size: 4rem;
  margin: 0;
  margin-right: -40vw;
  padding: 0;
  color: var(--color-header);
}

.s2 .cl2 .cl2-imginner {
    background: url("../../assets/img/s2_2.jpg");
  background-size: 180% auto;
  background-position: 55% 4%;
  background-repeat: no-repeat;
  padding: 60%;
}

.s2 .cl2 .s2_2 {
  max-width: 320px;
  margin: 2rem 1rem 0;
}

.s2 .cl3 .cl3-imginner {
    background: url("../../assets/img/s2_3.jpg");
  background-size: 140% auto;
  background-position: 70% 30%;
  background-repeat: no-repeat;
  padding: 60%;
}

.s2 .cl3 .s2_3 {
  width: 22vw;
  max-width: 360px;
  margin: 10rem 0 10rem auto;
}

@media screen and (min-width: 53em) {
  .s2 {
    display: grid;
    grid-template-areas: "cl1 cl2 cl3";
    grid-template-columns: 32% 38% 30%;
    position: relative;
  }
  .s2 .cl1 {
    grid-area: cl1;
    padding: 0 1rem;
  }
  .s2 .cl2 {
    grid-area: cl2;
    padding: 0 3rem;
  }
  .s2 .cl3 {
    grid-area: cl3;
    padding: 0 1rem;
  }
  .s2 .cl1 .cl1-txt .header {
    font-size: 3rem;
    margin: 4rem 0 0;
    padding: 0;
    color: var(--color-header);
  }
  .s2 .cl2 .cl2-txt .header {
    font-size: 5rem;
    margin: 0;
  }

  .s2 .cl2 .s2_2 {
    margin: 4rem auto 0;
  }
}
</style>