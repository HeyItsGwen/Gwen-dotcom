<script>
	//

	import Footer from './Footer.svelte';
	import About from './About.svelte';
	import Projects from './Projects.svelte';
	import Contact from './Contact.svelte';

	export let darkmode;
	let modeCheck;
	//wait for page to load so it can get an elements id
	window.addEventListener('load',e=>{
		//get element that controls dark/light mode
		modeCheck = document.getElementById('modeSwitcher');
		//make darkmode true if the switch is on, false if it's off
		darkmode=modeCheck.checked?true:false;
	})
	//function that changes the color mode (dark or light) based the state of the darkmode variable
	export const modeSwap = () => {
		darkmode?darkmode=false:darkmode=true;
	}
</script>

<nav class='d-flex justify-content-between'>
	<h1>Gwen.</h1>
	<!-- toggle for dark/light mode -->
	<div class="custom-control custom-switch modeToggle">
		<input type="checkbox" class="custom-control-input" id="modeSwitcher" on:click={modeSwap}>
		<label class="custom-control-label" for="modeSwitcher">light mode</label>
	</div>
</nav>

<main class='d-flex flex-column align-items-start'>
	<p></p>
	<About/>
	<Projects/>
	<Contact/>
</main>

<Footer/>

{#if !darkmode}
	<style>
		body {
			background-color: #081111;
			color: #E2FFFF;
		}
	</style>
{:else}
	<style>
		body {
			background-color: #F0FFFF;
			color: #081111;
		}
	</style>
{/if}

<style>
	:global(body) {
		padding: 0;
	}
	nav {
		padding: 5px;
		height: 50px;
	}

	nav .modeToggle {
		margin: 16px 10px;
	}

	nav h1 {
		text-transform: uppercase;
		font-weight: 100;
		margin-left: 10px;
	}

	main ::before {
		content:'';
		position: absolute;
		width: 30%;
		right: 34%;
		top: 60px;
		border-bottom: 1px solid rgb(202, 127, 139);
	}

	main {
		text-align: center;
		margin: 0 auto;
		padding: 20px 10px;
		width: 100%;
	}
</style>