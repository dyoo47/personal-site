<script lang="ts">
	export let href: string;
	export let onclick: () => void = () => {};
</script>

<a class="group flex items-center my-6" {href} on:click={onclick}>
	<hr class="inline mr-2 h-px w-8 group-hover:w-16 transition-width duration-150 ease-in-out" />
	<span
		class="text-xs tracking-widest font-bold text-slate-400 transition group-hover:text-primary-50"
	>
		<slot />
	</span>
</a>
