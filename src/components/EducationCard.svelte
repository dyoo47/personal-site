<script lang="ts">
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
	<div class="col-span-1">
		<span class="text-xs font-semibold text-slate-400">{span.toUpperCase()}</span>
		<br />
		<span class="text-xs font-semibold text-slate-400">{location.toUpperCase()}</span>
	</div>
	<div class="col-span-3">
		<h6 class="h6 text-primary-50">
			{title}
		</h6>
		<p class="text-sm">
			{description}
		</p>
	</div>
</a>
