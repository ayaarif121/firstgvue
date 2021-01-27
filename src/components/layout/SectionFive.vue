<template>
  <div class="section s5" data-scroll-section>
    <div class="s5-header" data-scroll data-scroll-speed="1">
      <div class="header">Would you like to become a model?</div>
    </div>
    <div class="s5-form">
      <input class="s5-input" name="name" placeholder="Name" />
      <input class="s5-input" name="email" placeholder="E-mail" />
      <input class="s5-input" name="phone" placeholder="Phone" />
      <div class="s5-action">
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
  name: "SectionFive",
};
</script>

<style scoped>
.s5 {
  grid-area: s5;
  display: grid;
  grid-template-areas: "heading" "form";
  position: relative;
}
.s5 .s5-header {
  font-size: calc(2rem + 4vw);
  grid-area: heading;
}
.s5 .s5-form {
  grid-area: form;
  margin-top: 4vw;
}
.s5 .s5-action {
  margin-top: 2vw;
}
.s5 .s5-input {
  width: 100%;
  padding: 1rem 0;
  background-color: #8d1a00;
  color: white;
  border: none;
  outline: none;
  font-size: calc(0.8rem + 0.8vw);
  border-bottom: 1px solid white;
  margin: 2vh 0;
}

.s5 .s5-action .obj-button {
  margin-right: 0;
}

.s5 .s5-input::placeholder {
  color: #fff;
  font-family: "poppins";
  font-weight: 300;
}

@media screen and (min-width: 53em) {
  .s5 {
    display: grid;
    grid-template-areas: "heading form";
    grid-template-columns: 55% 45%;
  }
  .s5 .s5-form {
    margin-top: 0;
  }
}
</style>
