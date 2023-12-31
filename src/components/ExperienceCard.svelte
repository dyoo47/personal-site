<script lang="ts">
	import Fa from 'svelte-fa';
	import { faArrowRight, faLink } from '@fortawesome/free-solid-svg-icons';

	interface link {
		label: string;
		href: string;
	}

	export let skills: string[];
	export let links: link[] = [];
	export let image: string | undefined = undefined;
	export let location: string = '';
	export let title: string = '';
	export let crossed: string | undefined = undefined;
	export let description: string;
	export let span: string = '';
	export let href: string;
	export let disableLink: boolean = false;
	let target = disableLink ? '' : '_blank';
</script>

<a
	{href}
	{target}
	class="mb-2 group grid grid-cols-4 bg-opacity-0 bg-slate-600 hover:bg-opacity-40 p-4 rounded transition duration-150 ease-in-out"
>
	{#if image}
		<div
			class="col-span-1 max-md:hidden h-min mr-4 rounded-md border-slate-600 border-2 group-hover:border-slate-400 transition duration-150 ease-in-out overflow-hidden"
		>
			<img src={image} class="w-full" alt="Project preview" />
		</div>
	{:else}
		<div class="col-span-1 max-md:hidden">
			<span class="text-xs font-semibold text-slate-400">{span.toUpperCase()}</span>
			<br />
			<span class="text-xs font-semibold text-slate-400">{location.toUpperCase()}</span>
		</div>
	{/if}
	<div class="col-span-3 max-md:col-span-4">
		<h6 class="h6 text-primary-50 mb-2 whitespace-nowrap mt-[1px]">
			{title}
			{#if disableLink}
				<span class="badge variant-outline-surface rounded-md ml-2 text-slate-400"
					>Private Repo</span
				>
			{:else}
				<Fa
					icon={faArrowRight}
					rotate={-45}
					scale={0.8}
					class="inline ml-2 group-hover:translate-x-1 group-hover:-translate-y-1 transition duration-150"
				/>
			{/if}
			{#if crossed}
				<br />
				<s class="text-slate-400 leading-4">{crossed}</s>
			{/if}
		</h6>
		<p class="mb-2 text-sm">
			{description}
		</p>
		<div class="mb-2">
			<ul>
				{#each links as link}
					<li class="mr-4 inline-block">
						<a
							href={link.href}
							target="_blank"
							class="text-sm font-medium text-primary-50 hover:text-primary-300"
						>
							<Fa class="inline" icon={faLink} />
							{link.label}</a
						>
					</li>
				{/each}
			</ul>
		</div>
		<ul>
			{#each skills as skill}
				<li class="inline">
					<span class="badge text-secondary-400 mt-2 mr-1 variant-outline-secondary rounded-xl"
						>{skill}</span
					>
				</li>
			{/each}
		</ul>
	</div>
</a>
