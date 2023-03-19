<script>
	let dismissed = false
	let toggle = () => (dismissed = !dismissed)
</script>

{#if !dismissed}
	<div class="p-5 fixed top-5 left-5 bg-red-400 rounded-lg text-white">
		<h1 class="text-2xl font-semibold">This website in a <span class="font-bold">Work in Progress</span>.</h1>
		<p class="text-base">Please expect unfinished content, bugs or broken mechanics.</p>
		<button on:click={toggle} class="hover:underline text-white">Dismiss</button>
	</div>
{/if}
