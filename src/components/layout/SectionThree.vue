<template>
			<div class="section s3" data-scroll-section>
				<div class="s3-models" >
					<div class="hh1" data-scroll data-scroll-speed="0.2" >Lea Holzfuss</div>
					<div class="hh2" data-scroll data-scroll-speed="0.3" >Deimante</div>
					<div class="hh3" data-scroll data-scroll-speed="0.4" >Ana Beatriz Barros</div>
					<div class="hh4" data-scroll data-scroll-speed="0.5" >Marina Nery</div>
					<div class="hh5" data-scroll data-scroll-speed="0.6" >Georgina Grenville</div>
					<div class="hh6" data-scroll data-scroll-speed="0.7" >Sofia Mechetner</div>
					<div class="hh7" data-scroll data-scroll-speed="0.8" >Dasha Denisenko</div>
				</div>
			</div>
</template>

<script>
export default {
  name: "SectionThree",
};
</script>

<style scoped>
.s3 {
	grid-area: s3;
	position: relative;

}

.s3-models{
	display: grid;
	grid-template-areas: 
	'hh1'
	'hh2' 
	'hh3' 
	'hh4' 
	'hh5' 
	'hh6'
	'hh7';
	margin: auto;
	grid-area: models;
	
   /* border: 2px solid black;  */
}

.s3-models div{
	font-size: 2rem;
	margin-top: 4rem;
	text-align: center;
	padding: 0;
}

.s3-models div:nth-child(-n+2){
	margin-top:0;
}

@media screen and (min-width: 53em) {
    .s3 {
	grid-template-areas: 'models';
	position: relative;

}

.s3-models{
	display: grid;
	grid-template-areas: 
	'hh1 hh2'
	'hh3 hh3' 
	 'hh4 hh4' 
	 'hh5 hh5' 
	 'hh6 hh6' 
	 'hh7 hh7';
	
   /* border: 2px solid black;  */
}

.s3-models div{
	font-size: 4rem;
	margin-top: 5rem;
	text-align: unset;
}
.hh1{
	grid-area: hh1;
	margin-left: 6rem;
	margin-right: auto;
	
}

.hh2{
	grid-area: hh2;
	margin-left: 4rem;
	margin-right: auto;
}

.hh3{
	grid-area: hh3;
	margin-left: auto;
	margin-right: 16rem;
}

.hh4{
	grid-area: hh4;
	margin-left: 10rem;
	margin-right: auto;
}

.hh5{
	grid-area: hh5;
	margin-left: auto;
	margin-right: 13rem;
}

.hh6{
	grid-area: hh6;
	margin-left: 12rem;
	margin-right: auto;
}

.hh7{
	grid-area: hh7;
	margin-left: auto;
	margin-right: 15rem;
}

}
</style>