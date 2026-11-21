<script lang="ts">
	import './layout.css';
	import favicon from '#lib/assets/favicon.svg';
	import type { LayoutProps } from './$types';
	import Toggler from '#lib/components/Toggler.svelte';

	let { children }: LayoutProps = $props();
</script>

<div
	class="flex h-screen w-full flex-col items-center justify-center overflow-hidden bg-slate-100 dark:bg-zinc-950"
>
	<header
		class="flex h-12 w-full shrink-0 flex-row items-center justify-between border-b border-slate-200 px-6 text-sm dark:border-zinc-800"
	>
		<div>
			<a class=" font-normal text-neutral-700 dark:text-zinc-200" href="./"> @apranthilaka </a>
		</div>
		<Toggler />
	</header>

	<main class=" min-h-0 w-full flex-1">
		{@render children()}
	</main>
</div>
