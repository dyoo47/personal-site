<script lang="ts">
	import Fa from 'svelte-fa';
	import { faArrowRight } from '@fortawesome/free-solid-svg-icons';

	export let skills: string[];
	export let image: string | undefined = undefined;
	export let location: string = '';
	export let title: string = '';
	export let description: string;
	export let span: string = '';
	export let href: string;
</script>

<a
	{href}
	class="mb-2 group grid grid-cols-4 bg-opacity-0 bg-slate-600 hover:bg-opacity-40 p-4 rounded transition duration-150 ease-in-out"
>
	{#if image}
		<div
			class="h-min mr-4 rounded-md border-slate-600 border-2 group-hover:border-slate-400 transition duration-150 ease-in-out overflow-hidden"
		>
			<img src={image} class="w-full" alt="Project preview" />
		</div>
	{:else}
		<div class="col-span-1">
			<span class="text-xs font-semibold text-slate-400">{span.toUpperCase()}</span>
			<span class="text-xs font-semibold text-slate-400">{location.toUpperCase()}</span>
		</div>
	{/if}
	<div class="col-span-3">
		<h6 class="h6 text-primary-50 mb-2">
			{title}
			<Fa
				icon={faArrowRight}
				rotate={-45}
				scale={0.8}
				class="inline ml-2 group-hover:translate-x-1 group-hover:-translate-y-1 transition duration-150"
			/>
		</h6>
		<p class="mb-2 text-sm">
			{description}
		</p>
		<ul>
			{#each skills as skill}
				<li class="inline">
					<span class="badge mt-2 mr-1 variant-ghost-secondary rounded-xl">{skill}</span>
				</li>
			{/each}
		</ul>
	</div>
</a>
