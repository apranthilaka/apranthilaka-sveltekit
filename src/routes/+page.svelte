<script lang="ts">
	import { ArrowRight, CircleCheck } from '@lucide/svelte';
	import { fly } from 'svelte/transition';

	let animationState = $state(false);

	$effect(() => {
		animationState = true;
	});

	let quickWins = $state<
		Array<{
			projectName: string;
			figmaLink: string;
			isProjectComplete: boolean;
		}>
	>([
		{
			projectName: 'E-Com Layouts & Components',
			figmaLink:
				'https://www.figma.com/proto/Z1GQBa5WjvRMWcOXVUIdq4/Twitter---Neutral?node-id=62-611&viewport=-1140%2C617%2C0.37&t=IZn7f1pFv932tu9o-8&scaling=contain&content-scaling=responsive&page-id=59%3A1032&hide-ui=1',

			isProjectComplete: false
		},
		{
			projectName: 'StackStore - Casestudy & Concepts',
			figmaLink:
				'https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Desktop-Designs?node-id=2004-826&viewport=-2124%2C252%2C0.15&t=fsHvNtdhL4gF0ZKc-8&scaling=contain&content-scaling=responsive&starting-point-node-id=1910%3A430&page-id=1834%3A4620&hide-ui=1',

			isProjectComplete: true
		},
		{
			projectName: 'SaaS Pipeline Management Workspace',
			figmaLink:
				'https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Desktop-Designs?node-id=1917-14051&viewport=215%2C487%2C0.45&t=MGgVuDyUQZHEUZWa-8&scaling=contain&content-scaling=responsive&page-id=0%3A1&hide-ui=1',
			isProjectComplete: false
		},
		{
			projectName: 'Obrand - Internal mail client',
			figmaLink:
				'https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Desktop-Designs?node-id=1917-12235&viewport=-337%2C-104%2C0.44&t=lryQMfwUEfq7UQvd-8&scaling=contain&content-scaling=responsive&page-id=1914%3A4181&hide-ui=1',
			isProjectComplete: false
		},
		{
			projectName: 'Kaleora - User Onboarding Flow',
			figmaLink:
				'https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Desktop-Designs?node-id=1917-15178&t=QqyKXTZeYd1Dd9uV-8&scaling=contain&content-scaling=responsive&page-id=1914%3A7342&hide-ui=1',
			isProjectComplete: false
		}
	]);
</script>

<div
	class="hide-scrollbar flex h-full flex-1 items-start justify-center overflow-y-auto bg-cover bg-center bg-no-repeat text-center text-neutral-600 md:items-center md:justify-center md:pb-0"
>
	{#if animationState}
		<div
			in:fly={{ y: 20, duration: 800 }}
			id="myDiv"
			class="flex h-max w-full shrink-0 flex-col items-center justify-start p-5 md:w-140 md:justify-center lg:items-center"
		>
			<!-- logo  -->
			<div class="mb-5 flex h-auto w-full flex-col text-center">
				<div>
					<div class="rotate-y-180 text-2xl">🦄</div>
					<div class="text-lg font-semibold text-slate-950 dark:text-zinc-200">@apranthilaka</div>
				</div>
				<div class="dark:text-orange-600">Product Designer & Developer [UI/UX]</div>
			</div>
			<!-- logo  -->

			<!-- Intro  -->
			<div class="mb-8 w-full">
				<div class="text-base text-sm leading-5 dark:text-zinc-400">
					Hey, I'm Aravinda. I design and develop digital products people actually enjoy using.
					Currently available for remote full-time roles and contract collaborations with companies
					and startups.
				</div>
			</div>
			<!-- Intro  -->

			<!-- projects  -->
			<div class=" flex w-full flex-col items-start justify-start">
				<!-- <p class=" mb-2 text-sm dark:text-zinc-600">Latest Projects</p> -->
				{#each quickWins as win (win.projectName)}
					<div
						class="flex h-10 w-full flex-row items-center justify-between border-b border-slate-300 dark:border-b-zinc-900 dark:text-zinc-400"
					>
						<div class="flex flex-row items-center gap-2 text-sm">
							<div>
								{win.projectName}
							</div>
							{#if win.isProjectComplete}
								<span class="mt-1 text-green-700 dark:text-green-500">
									<CircleCheck size="14" />
								</span>
							{/if}
						</div>
						<div class="flex flex-row items-center gap-1">
							<a
								class="text-sm underline hover:font-medium hover:text-neutral-950 dark:text-orange-500"
								target="_blank"
								href={win.figmaLink}
							>
								View Design
							</a>
						</div>
					</div>
				{/each}
			</div>
			<!-- projects  -->

			<!-- main links  -->
			<div
				class="mt-10 grid h-auto w-full grid-cols-[repeat(auto-fit,minmax(150px,1fr))] gap-2 md:grid-cols-[repeat(auto-fit,minmax(100px,1fr))]"
			>
				<a
					href="https://dribbble.com/aravinda"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center border border-neutral-300 px-3 py-2 text-sm hover:text-neutral-900 dark:border-zinc-800 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					Quick Wins
				</a>
				<a
					href="https://components.apranthilaka.workers.dev/"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center border border-neutral-300 px-3 py-2 text-sm hover:text-neutral-900 dark:border-zinc-800 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					Dev Lab
				</a>
				<a
					href="https://www.linkedin.com/in/aravindaprabath/"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center border border-neutral-300 px-3 py-2 text-sm hover:text-neutral-900 dark:border-zinc-800 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					LinkedIn
				</a>

				<a
					href="mailto:apranthilaka@gmail.com,apranthilaka@outlook.com"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center border border-neutral-200 px-3 py-2 text-sm hover:text-neutral-900 dark:border-zinc-800 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					Get in contact
				</a>

				<!-- <a
          href="https://github.com/apranthilaka"
          target="_blank"
          rel="noopener noreferrer"
          class="border border-white/30 rounded-sm hover:bg-black/10 hover:text-neutral-50 flex justify-center items-center h-fit px-3 py-2 w-full"
        >
          Github
        </a> -->

				<!-- <a
					href="https://wa.me/94777499801"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:text-neutral-900 dark:border-zinc-900 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					Whatsapp
				</a> -->
				<!--
				<a
					href="https://t.me/apranthilaka"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:text-neutral-900 dark:border-zinc-900 dark:text-zinc-400 hover:dark:text-zinc-200"
				>
					Telegram
				</a> -->
			</div>
			<!-- main links   -->
		</div>
	{/if}
</div>

<style>
	/* .disableFigmaLink {
		cursor: not-allowed;
	}
	.disableDevLink {
		cursor: not-allowed;
	} */

	.hide-scrollbar {
		scrollbar-width: none; /* Firefox */
		-ms-overflow-style: none; /* old Edge/IE */
	}
	.hide-scrollbar::-webkit-scrollbar {
		display: none; /* Chrome, Safari, mobile browsers */
	}
</style>
