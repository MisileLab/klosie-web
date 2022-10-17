<svelte:head>
<title>{title}</title>
</svelte:head>

<script>
	export let title = "klosie's web!";
	import { reveal } from 'svelte-reveal';
	import { fly } from 'svelte/transition';
	let visible = {
		projects2022: false
	};
	let flyx = -40;
</script>

<h1 use:reveal={{ transition: "slide", reset: true, duration: 500 }}>klosie, misile's cat!</h1>
<projectstitle use:reveal={{ transition: "slide", reset: true, duration: 1700}}>projects</projectstitle>
<details id="details" use:reveal={{ transition: "slide", reset: true, duration: 2500}} bind:open={visible["projects2022"]}>
	<summary>2022</summary>
	{#if visible["projects2022"]}
		<a transition:fly="{{ x: flyx, duration: 1000 }}">pull request check</a>
	{/if}
</details>
<donatestitle use:reveal={{ transition: "slide", reset: true, duration: 1700}}>Donate me</donatestitle>
<div class="donate">
	<a use:reveal={{ transition: "slide", reset: true, duration: 2500}} href="https://toss.me/klosie">Toss</a>
</div>
<style>
	#details {
		margin-left: 17.4%;
		font-size: 1.5em;
		color: #6F38C5;
	}

	.donate {
		margin-left: 17.4%;
		font-size: 1.5em;
	}

	projectstitle {
		display: block;
		color: #87A2FB;
		font-size: 1.7em;
		margin: auto;
		margin-top: 50px;
		margin-left: 17.4%;
	}

	donatestitle {
		display: block;
		color: #87A2FB;
		font-size: 1.7em;
		margin: auto;
		margin-top: 50px;
		margin-left: 17.4%;
	}

	h1 {
		color: #87A2FB;
		font-size: 3em;
		font-weight: 100;
		text-align: center;
		display: block;
		margin: auto;
		margin-top: 10px;
	}

	a {
		display: block;
	}

	:global(body) {
		background-color: #ADDDD0;
		font-weight: 100;
	}
</style>
