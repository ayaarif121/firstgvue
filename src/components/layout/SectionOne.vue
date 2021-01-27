<template>
  <div class="section s1">
    <div class="s1-images">

      <div class="s1-img" v-for="item in items" :key="item.className" :class="item.className" v-on:mouseover="mouseOn(item.className);" v-on:mouseleave="mouseOff(item.className)">
        <div class="s1-imginner"></div>
      </div>

    <!--  <div class="s1-img s1_1"  v-on:mouseover="mouseOn()">
        <div class="s1-imginner"></div>
      </div>
      <div class="s1-img s1_2"  v-on:mouseover="mouseOn()">
        <div class="s1-imginner"></div>
      </div>
      <div class="s1-img s1_3"  v-on:mouseover="mouseOn()">
        <div class="s1-imginner"></div>
      </div> -->

      <div class="s1-img s1_4 s1-txt">
        <div class="s1-imginner">
          Each day I am thankful for nights that turned into mornings friends
          that turned into family, and dreams that turned into reality
        </div>
      </div>
    </div>

    <div class="circle-path">
      <div class="obj">
        <div class="obj-circle">
          <img src="../../assets/svg/aa2.svg" />
        </div>
        <div class="obj-text">
          <h3>Fashion</h3>
          <p>
            The sixties: the years of youth protests, of sexual revolution, of
            women’s raise of consciousness and people wearing jeans instead of
            formal evening dresses at La Scala.
          </p>
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
  </div>
</template>



<script>
import gsap from 'gsap';

export default {

  name: "SectionOne",
  data: function() {
    return {
        items : [
          {className:"s1_1"},
          {className:"s1_2"},
          {className:"s1_3"}
        ]
    }
  
  },
  mounted: function() {
  },

  methods: {
    mouseOn: function(el){
      console.log(el);
      
          gsap
          .timeline({defaults: {duration: 1, ease: 'expo'}})
          .to("."+el, {scale: 0.9})
          .to("."+el+" .s1-imginner", {scale: 1.2, stagger: {from: 'center'}},0)
      
    },
    mouseOff: function(el){
      console.log(el);
      
          gsap
          .timeline({defaults: {duration: 1, ease: 'expo'}})
          .to("."+el, {scale: 1})
          .to("."+el+" .s1-imginner", {scale: 1, stagger: {from: 'center'}},0)
      
    }
  }

}
</script>

<style scoped>
.s1 {
  grid-area: s1;
  position: relative;
  margin-top: 0;
}

.s1-images {
  display: grid;
  grid-template-areas: "tx tx tx" "ssa ssb ssc";

  grid-template-columns: 30% 30% 30%;

  justify-content: center;
}

.s1_4 {
  grid-area: tx;
  width: 100%;
  max-width: 500px;
  font-size: 1rem;
  text-align: center;
  margin: 1rem auto;
}

.s1_1 {
  grid-area: ssa;
  width: calc(100vw - 70vw);
  max-width: 280px;
  z-index: 4;
  margin-top: 2rem;
  padding: 0 0.2rem;
}
.s1_2 {
  grid-area: ssb;
  width: calc(100vw - 70vw);
  max-width: 420px;
  z-index: 2;
  padding: 0 0.2rem;
}
.s1_3 {
  grid-area: ssc;
  width: calc(100vw - 70vw);
  max-width: 250px;
  margin-top: 3rem;
  padding: 0 0.2rem;
}

.s1-img {
  overflow: hidden;
}

.s1_1 .s1-imginner {
  background: url("../../assets/img/s1_1.jpg");
  background-size: cover;
  background-position: -110px -80px;
  width: 180%;
  padding: 50%;
}
.s1_2 .s1-imginner {
  background: url("../../assets/img/s1_2.jpg");
  background-size: cover;
  background-position: 50% 50%;
  width: 100%;
  padding: 50%;
}
.s1_3 .s1-imginner {
  background: url("../../assets/img/s1_3.jpg");
  background-size: cover;
  background-position: -150px -32px;
  width: 220%;
  padding: 54%;
}

.s1 .circle-path {
  display: flex;
  justify-content: center;
  z-index: 1000;
  color: var(--color-header);

  position: relative;
  top: -60px;
}

.s1 .circle-path .obj {
  width: 90vw;
  max-width: 800px;
  display: grid;
  grid-template-areas: "circle";
}
.s1 .circle-path .obj .obj-circle {
  grid-area: cicle;
}
.s1 .circle-path .obj .obj-text {
  grid-area: cicle;
  width: 60%;
  max-width: 800px;
  text-align: center;
  margin: auto;
  font-size: 0.8rem;
}
p {
  font-family: poppins;
  color: white;
}
.s1 .obj-button {
  width: 18vw;
}

.s1 .circle-path .obj .txt_ {
  font-size: 8rem;
}

@media screen and (min-width: 53em) {
  .s1-images {
    display: flex;
    max-width: 90vw;
    margin: auto;
    position: relative;
    top: 50px;

    /* border: 2px solid black;  */
  }

  .s1_1 {
    grid-area: unset;
    padding: unset;
    z-index: 4;
    margin-top: 7rem;
  }
  .s1_2 {
    height: 300px;
    position: relative;
    left: -50px;
    z-index: 2;
  }
  .s1_3 {
    grid-area: unset;
    padding: unset;
    position: relative;
    left: -30px;
    margin-top: 4rem;
  }

  .s1_4 {
    grid-area: unset;
    padding: unset;
    position: relative;
    left: -88px;
    font-size: 1.6rem;
    text-align: start;
  }

  .s1_1 .s1-imginner {
    background-size: cover;
    background-position: -110px -80px;
    width: 180%;
    padding: 50%;
  }
  .s1_2 .s1-imginner {
    background-size: cover;
    background-position: 50% 50%;
    width: 100%;
    padding: 50%;
  }
  .s1_3 .s1-imginner {
    background-size: cover;
    background-position: -150px -32px;
    width: 220%;
    padding: 54%;
  }

  .s1 .circle-path {
    position: relative;
    top: -100px;
  }

  .s1 .circle-path .obj .obj-text {
    font-size: 1rem;
  }
}
</style>