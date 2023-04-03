<script lang='ts'>
	import '../app.postcss';
	import { BottomNav, BottomNavItem, Tooltip } from "flowbite-svelte"
	import { stringify } from 'postcss';
	import Photo from 'svelte-heros-v2/Photo.svelte';
	import Home from 'svelte-heros-v2/Home.svelte';

</script>

<main style="height: 100%">
	<slot />
</main>

<BottomNav position="fixed" innerDiv="grid-cols-2">
	<BottomNavItem btnName="Home" appBtnPosition="left">
		<a href="/">
			<Home />
			<Tooltip arrow={false}>Home</Tooltip>
		</a>
	</BottomNavItem>

	<BottomNavItem btnName="Gallery" appBtnPosition="right">
		<a href="gallery">
			<Photo />
			<Tooltip arrow={false}>Gallery</Tooltip>
		</a>
	</BottomNavItem>
</BottomNav>

<style>

	body {
		height: calc(100vh - 64px);
		widows: 100vw;
	}
	a {
		width: 100%;
		height: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>