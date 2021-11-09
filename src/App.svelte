<script lang="ts">
	import Header from './Header.svelte'
	import Three from './Three.svelte'

	let pfp_url = "";
	let pfp_name = "test alt";
</script>

<main>
	<Header {pfp_url} {pfp_name}/>
	<Three/>
</main>

<style>
	main {
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		text-align: center;
		padding: 0;
		margin: 0;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>