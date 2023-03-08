<script>
	import Video from './nugget.mp4'
	import { onMount } from 'svelte'
	export let controller
	let vid
	let text
	onMount(() => {
		// Video Scene
		let accelamount = 0.1
		let scrollpos = 0
		let delay = 0

		let scene = new ScrollMagic.Scene({
			duration: 7000,
			triggerElement: '#trigger',
			triggerHook: 0,
		})
			.setPin('#trigger')
			.addTo(controller)

		scene.on('update', (e) => {
			scrollpos = e.scrollPos / 1000
		})

		setInterval(() => {
			delay += (scrollpos - delay) * accelamount

			vid = delay
		}, 33.3)

		// GOLD CHANGES EVERYTHING Animation
		let goldAnim1 = TweenMax.fromTo(text, 6, { opacity: 0 }, { opacity: 1 })
		let goldAnim2 = TweenMax.fromTo(text, 1, { opacity: 1 }, { opacity: 0 })
		let goldScene1 = new ScrollMagic.Scene({
			duration: 6000,
			triggerElement: '#trigger',
			triggerHook: 0,
		})
			.setTween(goldAnim1)
			.addTo(controller)
		let goldScene2 = new ScrollMagic.Scene({
			duration: 1000,
			triggerElement: '#trigger',
			offset: 6000,
			triggerHook: 0,
		})
			.setTween(goldAnim2)
			.addTo(controller)
	})
</script>

<div id="trigger" class="overflow-x-hidden">
	<video src={Video} bind:currentTime={vid} class="overflow-x-hidden object-cover z-0" />
	<div class="grid z-10 place-content-center absolute top-0 left-0 w-full h-full">
		<h1 class="text-6xl text-white opacity-0 z-10 font-display" bind:this={text} style="opacity: 0;">
			GOLD CHANGES EVERYTHING
		</h1>
	</div>
</div>
