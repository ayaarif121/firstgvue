<template>
  <main data-scroll-container>
   <!-- <img alt="Vue logo" src="./assets/logo.png">
    -->
      <Header @mycursor="cursor"/>
      <SectionOne v-if="sec1"/>
      <SectionTwo/>
      <SectionThree/>
      <SectionFour/>
      <SectionFive/>
      <svg ref="svgx" class="cursor" width="30" height="30" viewBox="0 0 30 30">
        <circle class="cursor__inner" cx="15" cy="15" r="7.5" />
      </svg>
  </main>
</template>

<script>




import Header from './components/layout/Header';
import SectionOne from './components/layout/SectionOne';
import SectionTwo from './components/layout/SectionTwo';
import SectionThree from './components/layout/SectionThree';
import SectionFour from './components/layout/SectionFour';
import SectionFive from './components/layout/SectionFive';
import Cursoor from './components/Cursoor';
import Cursor from './assets/js/cursor';

export default {
  name: 'App',
  components: { 
    Header,
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFour,
    SectionFive,
    Cursoor,
    Cursor


  },
  data: () => {
    return{
      sec1 : true,
      mouse: {x: 0, y: 0},
      cursor: {},
    }
  },
  mounted(){
    this.getMousePos();
    
  },
  methods:{
     getMousePos(){
       this.cursor = new Cursor();
       console.log(this.cursor);
    }


  }
}

</script>

<style>
  *,
  *::after,
  *::before {
    box-sizing: border-box;
  }

  :root {
    font-size: 15px;
  }

  @font-face {
    font-family: lightfont;
    src: url(./assets/fonts/Lighthaus.otf);
    }

  body {
    margin: 0;
    --color-text: #fff;
    --color-bg: #8D1A00;
      --color-header: #FFACB9;
      --color-link: #fff;
    --color-link-hover: #FFACB9;
    color: var(--color-text);
    background-color: var(--color-bg);
    --cursor-stroke: none;
    --cursor-fill: #c5681c;
    --cursor-stroke-width: 1px;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-family: lightfont;
    --cursor-stroke: #ffffff;
    --cursor-fill: none;
    --cursor-stroke-width: 1px;
    
  }
  main {
    display: grid;
    grid-template-areas: 'nav' 's1' 's2' 's3' 's4' 's5';
    width: 90%;
    margin: 0 auto;
  }
  .section{
	  -webkit-margin: 14vh 0;
    margin: 14vh 0;
  }
  p{

    font-family: poppins;
    color: white;
      
  }
  .obj-button {
    display: grid;
    grid-template-areas: "button";
    width: 20vw;
    max-width: 120px;
    margin: auto;
  }
  .obj-button .continue {
    grid-area: button;
  }
  .obj-button .arrow {
    grid-area: button;
    width: 45%;
    margin: auto;
  }


  @media screen and (min-width:53em) {
    :root {
      font-size: 18px;
    }
  }


    @media (any-pointer: fine) {
	.cursor {
		position: fixed;
		top: 0;
		left: 0;
		display: block;
		pointer-events: none;
		z-index: 9999;
	}
	.cursor__inner {
		fill: var(--cursor-fill);
		stroke: var(--cursor-stroke);
		stroke-width: var(--cursor-stroke-width);
		opacity: 1;
	}
	.no-js .cursor {
		display: none;
	}
}

</style>
