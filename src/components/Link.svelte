<script lang="ts">
	export let href: string;
</script>

<a class="group flex items-center my-4" {href}>
	<hr class="inline mr-2 h-px w-8 group-hover:w-16 transition-width duration-150 ease-in-out" />
	<span class="font-mono font-bold text-slate-400 transition group-hover:text-primary-50"
		><slot /></span
	>
</a>
