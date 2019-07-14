<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<svelte:head>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/bootswatch/4.3.1/lux/bootstrap.min.css" integrity="sha256-2AE13SXoJY6p0WSPAlYEZpalYyQ1NiipAwSt3s60n8M=" crossorigin="anonymous" />
</svelte:head>

<Nav {segment}/>

<main class="jumbotron">
	<slot />
</main>