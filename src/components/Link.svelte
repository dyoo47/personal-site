<script lang="ts">
	export let href: string;
</script>

<a class="group flex items-center w-fit py-3" {href}>
	<span
		class="mr-4 h-px w-8 bg-slate-400 transition-all group-hover:w-16 group-hover:bg-primary-50 group-focus-visible:w-16 group-focus-visible:bg-primary-50"
	/>
	<span
		class="text-xs tracking-widest font-bold text-slate-400 transition group-hover:text-primary-50 group-focus-visible:text-primary-50"
	>
		<slot />
	</span>
</a>
