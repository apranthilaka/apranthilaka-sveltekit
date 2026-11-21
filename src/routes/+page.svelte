<script>
	import { fly } from 'svelte/transition';

	let animationState = $state(false);

	$effect(() => {
		animationState = true;
	});
</script>

<div
	class="modern-scrollbar flex h-screen w-full overflow-y-auto bg-slate-100 bg-cover bg-center bg-no-repeat text-center text-sm text-neutral-600 md:items-center md:justify-center md:p-2 dark:bg-zinc-950"
>
	{#if animationState}
		<div
			in:fly={{ y: 20, duration: 800 }}
			id="myDiv"
			class="flex h-auto w-full flex-col justify-center overflow-auto bg-white/30 p-10 shadow-sm md:w-140 md:justify-between md:rounded-md"
		>
			<!-- logo  -->
			<div class="mb-5 flex h-auto w-full flex-col text-center">
				<div>
					<span class="inline-flex items-center text-lg">
						<span class="text-lg font-semibold">@apranthilaka</span>
					</span>
				</div>
				<div>Product Design Engineer (UI/UX)</div>
			</div>
			<!-- logo  -->

			<!-- Intro  -->
			<div class="mb-8 w-full">
				<div>
					Hey, I'm Aravinda. I design and build digital products people actually enjoy using.
					Currently vailable for remote full-time roles and contract collaborations with companies
					and startups.
				</div>
			</div>
			<!-- Intro  -->

			<!-- main links  -->
			<div class="grid w-full grid-cols-[repeat(auto-fit,minmax(150px,1fr))] gap-2">
				<a
					href="https://dribbble.com/aravinda"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:bg-neutral-100 hover:text-neutral-900"
				>
					<!-- <i class="ph ph-dribbble-logo" aria-hidden="true"></i> -->
					Design
				</a>
				<a
					href="https://components.apranthilaka.workers.dev/"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:bg-neutral-100 hover:text-neutral-900"
				>
					Development
				</a>
				<a
					href="https://www.linkedin.com/in/aravindaprabath/"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:bg-neutral-100 hover:text-neutral-900"
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
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:bg-neutral-100 hover:text-neutral-900"
				>
					<!-- <i class="ph ph-file-text" aria-hidden="true"></i> CV -->
					Whatsapp
				</a>

				<a
					href="https://t.me/apranthilaka"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:bg-neutral-100 hover:text-neutral-900"
				>
					Telegram
				</a>
				<a
					href="mailto:apranthilaka@gmail.com,apranthilaka@outlook.com"
					target="_blank"
					rel="noopener noreferrer"
					class="flex h-fit w-full items-center justify-center rounded-sm border border-neutral-300 px-3 py-2 hover:bg-neutral-100 hover:text-neutral-900"
				>
					<!-- <i class="ph ph-file-text" aria-hidden="true"></i> CV -->
					Email
				</a>
			</div>
			<!-- main links   -->

			<!-- projects  -->
			<div class="mt-5 flex w-full flex-col items-start justify-start">
				<p class="mt-5 mb-2 text-sm text-neutral-400">Selected Projects</p>
				<div>
					<div class="inline-block pr-2">
						<a
							class="text-left underline"
							target="_blank"
							href="https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Desktop-Designs?node-id=2004-826&viewport=-2124%2C252%2C0.15&t=fsHvNtdhL4gF0ZKc-8&scaling=contain&content-scaling=responsive&starting-point-node-id=1910%3A430&page-id=1834%3A4620&hide-ui=1"
						>
							StackStore
						</a>
					</div>

					<!-- <div class="inline-block pr-2">
            <a
              class="text-left underline"
              target="_blank"
              href="https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Dribble-Desktop-Designs?node-id=1651-3403&viewport=475%2C428%2C0.16&t=CPdshzj8QYtL577s-8&scaling=contain&content-scaling=responsive&starting-point-node-id=2%3A437&page-id=0%3A1&hide-ui=1"
            >
              Obrand
            </a>
          </div>

          <div class="inline-block pr-2">
            <a
              class="text-left underline"
              target="_blank"
              href="https://www.figma.com/proto/OiECY5HRCcUmrRlP5ZVQXa/Dribble-Desktop-Designs?node-id=1651-4779&viewport=475%2C428%2C0.16&t=CPdshzj8QYtL577s-8&scaling=contain&content-scaling=responsive&starting-point-node-id=2%3A437&page-id=0%3A1&hide-ui=1"
            >
              Kaleora
            </a>
          </div> -->
				</div>
			</div>
			<!-- projects  -->
		</div>
	{/if}
</div>
