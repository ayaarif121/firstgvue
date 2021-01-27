<template>

      <svg ref="svg" class="cursor" width="30" height="30" viewBox="0 0 30 30">
        <circle class="cursor__inner" cx="15" cy="15" r="7.5" />
      </svg>

</template>

<script>

import gsap from "gsap";

export default {
  name: 'Cursoor',
  props: ["mymouse"],
  data: () => {
    return{
        sec1 : true,
        bounds: {},
        mouse: {x: 0, y: 0},
        renderedStyles: {
            tx: {previous: 0, current: 0, amt: 0.2},
            ty: {previous: 0, current: 0, amt: 0.2},
            scale: {previous: 1, current: 1, amt: 0.2},
            opacity: {previous: 1, current: 1, amt: 0.2}
        },
        
    }
  },
  created(){
        
        //window.addEventListener('mousemove', this.onMouseMoveEv);
        this.onMouseMoveEv();
        this.bounds = this.$refs.svg.getBoundingClientRect();

  },

  methods:  {
    onMouseMoveEv(){

           /* this.renderedStyles.tx.previous = this.renderedStyles.tx.current = this.mymouse.x - this.bounds.width/2;
            this.renderedStyles.ty.previous = this.renderedStyles.ty.previous = this.mymouse.y - this.bounds.height/2;
            gsap.to(this.$refs.svg, {duration: 0.9, ease: 'Power3.easeOut', opacity: 1});
            requestAnimationFrame(() => this.render());
            window.removeEventListener('mousemove', this.onMouseMoveEv); */
            console.log(this.mymouse);

        },
    enter() {
        this.renderedStyles['scale'].current = 2;
        this.renderedStyles['opacity'].current = 0.3;
    },

    leave() {
        this.renderedStyles['scale'].current = 1;
        this.renderedStyles['opacity'].current = 1;
    },
    
    render() {
        this.renderedStyles['tx'].current = this.mymouse.x - this.bounds.width/2;
        this.renderedStyles['ty'].current = this.mymouse.y - this.bounds.height/2;

        for (const key in this.renderedStyles ) {
            this.renderedStyles[key].previous = lerp(this.renderedStyles[key].previous, this.renderedStyles[key].current, this.renderedStyles[key].amt);
        }
                    
        this.$refs.svg.style.transform = `translateX(${(this.renderedStyles['tx'].previous)}px) translateY(${this.renderedStyles['ty'].previous}px) scale(${this.renderedStyles['scale'].previous})`;
        this.$refs.svg.style.opacity = this.renderedStyles['opacity'].previous;

        requestAnimationFrame(() => this.render());
    }

    
  }
}

</script>

<style scoped>
 
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
