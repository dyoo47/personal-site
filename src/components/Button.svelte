<script lang="ts">
	export let href: string;
</script>

<a class="h3 mr-5 opacity-60 transition duration-300 ease-in-out hover:opacity-100" {href}>
	<slot />
</a>
