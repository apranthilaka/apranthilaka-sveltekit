<script>
	import { fly } from 'svelte/transition';

	let animationState = $state(false);

	$effect(() => {
		animationState = true;
	});

	let quickWins = $state([
		{
			projectName: 'StackStore',
			figmaLink:
				'https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Desktop-Designs?node-id=2004-826&viewport=-2124%2C252%2C0.15&t=fsHvNtdhL4gF0ZKc-8&scaling=contain&content-scaling=responsive&starting-point-node-id=1910%3A430&page-id=1834%3A4620&hide-ui=1',
			devLink: 'https://components.apranthilaka.workers.dev/projectone',
			disableFigmaLink: false,
			disableDevLink: false
		},
		{
			projectName: 'Metafull',
			figmaLink:
				'https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Desktop-Designs?node-id=2042-2122&viewport=590%2C422%2C0.25&t=jrI4MoCWCYDFPbN2-8&scaling=contain&content-scaling=responsive&page-id=0%3A1&hide-ui=1',
			devLink: 'https://components.apranthilaka.workers.dev/projectone',
			disableFigmaLink: true,
			disableDevLink: true
		},
		{
			projectName: 'StackStore3',
			figmaLink:
				'https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Desktop-Designs?node-id=2004-826&viewport=-2124%2C252%2C0.15&t=fsHvNtdhL4gF0ZKc-8&scaling=contain&content-scaling=responsive&starting-point-node-id=1910%3A430&page-id=1834%3A4620&hide-ui=1',
			devLink: 'https://components.apranthilaka.workers.dev/projectone',
			disableFigmaLink: true,
			disableDevLink: true
		}
	]);
</script>

<div
	class="modern-scrollbar flex h-screen w-full overflow-y-auto bg-cover bg-center bg-no-repeat text-center text-sm text-neutral-600 md:items-center md:justify-center md:p-2"
>
	{#if animationState}
		<div
			in:fly={{ y: 20, duration: 800 }}
			id="myDiv"
			class="flex h-auto w-full flex-col justify-center overflow-auto p-5 md:w-140 md:justify-between"
		>
			<!-- logo  -->
			<div class="mb-5 flex h-auto w-full flex-col text-center">
				<div>
					<div class="rotate-y-180 text-2xl">🦄</div>
					<div class="text-lg font-semibold text-slate-950 dark:text-zinc-200">@apranthilaka</div>
				</div>
				<div class="dark:text-orange-600">Product Design Engineer (UI/UX)</div>
			</div>
			<!-- logo  -->

			<!-- Intro  -->
			<div class="mb-8 w-full">
				<div class="dark:text-zinc-400">
					Hey, I'm Aravinda. I design and build digital products people actually enjoy using.
					Currently vailable for remote full-time roles and contract collaborations with companies
					and startups.
				</div>
			</div>
			<!-- Intro  -->

			<!-- main links  -->
			<div
				class="grid w-full grid-cols-[repeat(auto-fit,minmax(120px,1fr))] gap-2 md:grid-cols-[repeat(auto-fit,minmax(150px,1fr))]"
			>
				<a
					href="https://dribbble.com/aravinda"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:text-neutral-900 dark:border-zinc-900 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					<!-- <i class="ph ph-dribbble-logo" aria-hidden="true"></i> -->
					Design
				</a>
				<a
					href="https://components.apranthilaka.workers.dev/"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:text-neutral-900 dark:border-zinc-900 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					Development
				</a>
				<a
					href="https://www.linkedin.com/in/aravindaprabath/"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:text-neutral-900 dark:border-zinc-900 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					<!-- <i class="ph ph-linkedin-logo" aria-hidden="true"></i> -->
					LinkedIn
				</a>

				<!-- <a
          href="https://github.com/apranthilaka"
          target="_blank"
          rel="noopener noreferrer"
          class="border border-white/30 rounded-sm hover:bg-black/10 hover:text-neutral-50 flex justify-center items-center h-fit px-3 py-2 w-full"
        >
          Github
        </a> -->

				<a
					href="https://wa.me/94777499801"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:text-neutral-900 dark:border-zinc-900 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					<!-- <i class="ph ph-file-text" aria-hidden="true"></i> CV -->
					Whatsapp
				</a>

				<a
					href="https://t.me/apranthilaka"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:text-neutral-900 dark:border-zinc-900 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					Telegram
				</a>
				<a
					href="mailto:apranthilaka@gmail.com,apranthilaka@outlook.com"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:text-neutral-900 dark:border-zinc-900 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					<!-- <i class="ph ph-file-text" aria-hidden="true"></i> CV -->
					Email
				</a>
			</div>
			<!-- main links   -->

			<!-- projects  -->
			<div class="mt-10 flex w-full flex-col items-start justify-start">
				<!-- <p class="mt-5 mb-2 text-sm dark:text-zinc-600">Latest Projects</p> -->
				{#each quickWins as win (win.projectName)}
					<div
						class="flex h-10 w-full flex-row items-center justify-between border-b border-slate-300 dark:border-b-zinc-900 dark:text-zinc-400"
					>
						<div>{win.projectName}</div>
						<div class="inline-flex gap-4">
							<a
								class={win.disableFigmaLink
									? 'cursor-not-allowed text-slate-400'
									: 'text-orange-500 hover:underline'}
								target="_blank"
								href={win.figmaLink}
							>
								Figma
							</a>
							<a
								// class:disableDevLink={win.disableDevLink}
								class={win.disableDevLink
									? 'cursor-not-allowed text-slate-400'
									: 'text-orange-500 hover:underline'}
								target="_blank"
								href={win.devLink}
							>
								Live
							</a>
						</div>
					</div>
				{/each}
			</div>
			<!-- projects  -->
		</div>
	{/if}
</div>

<style>
	.disableFigmaLink {
		cursor: not-allowed;
	}
	.disableDevLink {
		cursor: not-allowed;
	}
</style>
