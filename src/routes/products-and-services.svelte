<script>
	import Card from '../components/Card.svelte';

	import { ROUTER } from '../constants';

	const products = [
		{ label: "Dent Instruments", href: ROUTER.DENT },
		{
			label: "Dranetz",
			href: ROUTER.DRANETZ
		},
		{ label: "Electrotek Systems", href: ROUTER.ELECTROTEK },
		{ label: "Power Standards Lab", href: ROUTER.POWER_STANDARDS }
	];

	const services = [
		{ label: "Consultancy from IMH", href: ROUTER.CONSULTANCY_FROM_IMH }
	]
</script>

<svelte:head>
	<title>Products and Services</title>
</svelte:head>

<h3>Products and Services</h3>

<div class="container">
	<h4 class="text-muted">Products</h4>
	<div class="row">
	
		{#each products as { label, href }}
			<Card {href} text={label} title={label} />
		{/each}
	</div>
	<hr class="my-4" />
	<h4 class="text-muted">Services</h4>
	<div class="row">
		{#each services as { label, href }}
			<Card {href} text={label} title={label} />
		{/each}
	</div>
</div>
