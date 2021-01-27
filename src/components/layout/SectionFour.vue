<template>
  <div class="section s4" data-scroll-section>
    <div class="s4-img" data-scroll data-scroll-speed="0.8">
      <div class="s4-imginner"></div>
    </div>
    <div class="s4-txt">
      <div class="t1">Women</div>
      <div class="t2">Not every body could be a model</div>
      <div class="t3">
        <div class="obj-button">
          <div class="continue">
            <img src="../../assets/svg/continue.svg" />
          </div>
          <div class="arrow">
            <div>
              <img src="../../assets/svg/arrow.svg" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SectionFour",
};
</script>

<style scoped>
.s4 {
  grid-area: s4;
  display: grid;
  grid-template-areas: "img" "txt";
  position: relative;
}

.s4 .s4-img {
  grid-area: img;
}
.s4 .s4-img .s4-imginner {
    background: url("../../assets/img/s4.jpg");
  background-size: 100% auto;
  background-position: 0% 49%;
  background-repeat: no-repeat;
  padding: 32%;
}

.s4 .s4-txt {
  grid-area: txt;
  display: grid;
  grid-template-areas: "t1 t3" "t2 t3";
  grid-template-columns: 70% 30%;
  margin: 1rem auto;
  z-index: 1000;
}

.s4 .s4-txt .t1 {
  grid-area: t1;
  color: var(--color-header);
  font-size: calc(0.5rem + 2vw);
}
.s4 .s4-txt .t2 {
  grid-area: t2;
  font-size: 1.4rem;
}

.s4 .s4-txt .t3 {
  grid-area: t3;
  margin-right: 0;
}
.s4 .s4-txt .t3 .obj-button {
  margin-right: 0;
}

@media screen and (min-width: 53em) {
  .s4 {
    display: grid;
    grid-template-areas: "img txt";
    grid-template-columns: 60% 40%;
  }

  .s4 .s4-txt {
    grid-area: txt;
    display: block;
    margin: auto;
    margin-left: 2rem;
  }

  .s4 .s4-txt .t2 {
    grid-area: t2;
    font-size: 5rem;
    margin: 1rem;
    margin-left: -24vw;
  }

  .s4 .s4-txt .t3 .obj-button {
    margin-left: 0;
  }
}
</style>