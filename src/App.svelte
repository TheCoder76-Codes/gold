<script>
	import Video from './lib/Video.svelte'
	import Info from './lib/Info.svelte'
	import ReversedInfo from './lib/ReversedInfo.svelte'
	import './app.css'
	let controller = new ScrollMagic.Controller()
</script>

<main class="bg-black text-white">
	<Video bind:controller />
	<Info bind:controller />
	<ReversedInfo bind:controller />
</main>
