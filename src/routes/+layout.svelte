<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import ThemeSwitcher from './ThemeSwitcher.svelte';
	import { SvelteTheme } from 'svelte-themes';

	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<SvelteTheme enableSystem enableColorScheme defaultTheme="system" attribute="class">
	{@render children()}
	<ThemeSwitcher />
</SvelteTheme>
