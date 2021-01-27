<template>
    <div class="nav">
		<div class="nav__logo">
            <svg  width="30" height="30" viewBox="0 0 30 30">
                <circle class="" cx="15" cy="15" r="7.5"/>
            </svg>
		</div>
				<div class="nav__links">
					<a v-on:mouseover="Enter" href="https://tympanus.net/Development/InlineMenuLayout/">About</a>
					<a href="https://tympanus.net/codrops/?p=52018">Women</a>
                    <a href="https://github.com/codrops/ImageStackGrid/">Contact us</a>
                    <a href="https://github.com/codrops/ImageStackGrid/">Becaome a model</a>
		</div>
    </div>
</template>

<script>
export default {
	name: 'Header',
	props: ["mycursor"],
	mounted(){
		console.log(this.mycursor);
	},
	methods: {
		Enter(){
			console.log("this.mycursor");
		}
		
	}
}
</script>

<style scoped>
.nav {
	padding: 1rem;
	text-align: center;
	position: relative;
	z-index: 1000;
	grid-area: nav;
	align-items: center;
	max-width: 90vw;
	margin: 0 auto ;

}

.nav__logo {
	display: flex;
	justify-content: center;
	padding: 1rem ;
	
    
}

.nav__links {
	display: inline;
	margin: auto 0;

}

.nav__links a:not(:last-child) {
	margin-right: 1rem;
}
a {
	text-decoration: none;
	color: #ffffff;
	outline: none;
	font-size: 0.7rem;
}
a:hover,
a:focus {
	text-decoration: underline;
	color: #FFACB9;
	outline: none;
}

@media screen and (min-width:53em) {
	:root {
		font-size: 18px;
	}

	.nav {
		padding: 1.5rem 0rem;
		
		width: 100%;
		
		display: flex;
		
		justify-content: space-between;
		
	
		
	}

	.nav__logo {
		margin: 0;
	}

	.nav__links {
		padding: 0;
	}

	.nav a {
		font-size: 1rem;
		pointer-events: auto;
	}
}

</style>