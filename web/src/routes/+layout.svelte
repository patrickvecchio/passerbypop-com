<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Footer from '$lib/components/Footer.svelte';
	import Header from '$lib/components/Header.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>Passerby - Official Website</title>
</svelte:head>

<div class="flex justify-center">
	<div class="w-[600px]">
		<div class="mb-4"><Header /></div>
		<div
			class="w-[600px] h-[516px] bg-[url('/images/3d-bucking-bronco.png')] bg-center bg-no-repeat align-center content-center"
		>
			{@render children()}
		</div>
		<div class="mt-14"><Footer /></div>
	</div>
</div>
