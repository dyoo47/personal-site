<script lang="ts">
	export let location: string = '';
	export let title: string = '';
	export let description: string;
	export let span: string = '';
</script>

<span
	class="mb-2 lg:group grid grid-cols-4 bg-opacity-0 bg-slate-600 lg:hover:bg-opacity-40 px-4 lg:py-4 rounded transition duration-150 ease-in-out"
>
	<div class="col-span-1 max-md:hidden">
		<span class="text-xs font-semibold text-slate-400">{span.toUpperCase()}</span>
		<br />
		<span class="text-xs font-semibold text-slate-400">{location.toUpperCase()}</span>
	</div>
	<div class="col-span-3 max-md:col-span-4">
		<h6 class="h6 text-primary-50">
			{title}
		</h6>
		<p class="text-sm">
			{description}
		</p>
	</div>
</span>
