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
		class="flex h-14 w-full shrink-0 flex-row items-center justify-between border-b border-b-neutral-200 bg-slate-100 px-4 text-sm dark:border-b-zinc-900 dark:bg-zinc-950 dark:text-neutral-500"
	>
		<div>
			<a class=" font-normal text-neutral-700 dark:text-zinc-200" href="./"> @apranthilaka </a>
		</div>
		<Toggler />
	</header>

	<main class=" min-h-0 w-full flex-1">
		{@render children()}
	</main>
	<footer
		class="hidden flex-col items-center justify-center pb-7 text-sm text-slate-900 md:flex dark:text-zinc-500"
	>
		<div class="text-xs text-neutral-500">Powered by</div>
		<a
			class="text-xs text-orange-600 capitalize"
			href="https://www.youtube.com/watch?v=dQw4w9WgXcQ&list=RDdQw4w9WgXcQ&start_radio=1"
		>
			Claude AI Sites
		</a>
	</footer>
</div>
