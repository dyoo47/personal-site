<script lang="ts">
	export let skills: string[];
	export let location: string;
	export let title: string;
	export let description: string;
	export let span: string;
	export let href: string;
</script>

<a
	{href}
	class="mb-2 grid grid-cols-4 bg-opacity-0 bg-slate-600 hover:bg-opacity-40 p-4 rounded transition duration-150 ease-in-out"
>
	<div class="col-span-1">
		<span class="text-xs font-semibold text-slate-400">{span.toUpperCase()}</span>
		<span class="text-xs font-semibold text-slate-400">{location.toUpperCase()}</span>
	</div>
	<div class="col-span-3">
		<h6 class="h6 text-primary-50 mb-2">{title}</h6>
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
