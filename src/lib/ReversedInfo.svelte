<script>
	import { onMount } from 'svelte'
	export let controller
	let content
	onMount(() => {
		let contentAnim = TweenMax.fromTo(content, 1, { opacity: 0 }, { opacity: 1 })
		let contentScene = new ScrollMagic.Scene({
			duration: 800,
			triggerElement: content,
			triggerHook: 0.7,
		})
			.setTween(contentAnim)
			.addTo(controller)
		console.log(content.parentElement)
	})
</script>

<div bind:this={content} class="text-white p-10 z-20 flex items-center justify-center gap-10">
	<slot />
	<!-- <div class="relative">
		<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full">
			<h1 class="text-lg">Source 1: A photo of a gold nugget.</h1>
		</div>
		<img src="https://picsum.photos/600/300" alt="Gold." />
	</div>
	<div>
		<h1 class="text-4xl font-display">WHAT IS THE GOLD RUSH?</h1>
		<p class="text-base max-w-xl">
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus explicabo tempora commodi. Ad, quos
			reiciendis sapiente a ex mollitia beatae inventore voluptatum sed voluptates hic impedit ducimus enim
			officiis aliquid delectus quis unde natus doloribus qui? Natus aliquam quia repellat nobis accusamus ratione
			officia. Fugiat, in deleniti. Fuga labore deleniti recusandae esse consequatur dicta reprehenderit?
			Accusantium odio distinctio voluptatibus omnis molestias excepturi adipisci debitis accusamus consequatur
			voluptate mollitia quam nihil, perspiciatis quasi illo sapiente laboriosam cum ullam maxime, ratione tempora
			praesentium! Unde obcaecati eum distinctio quaerat sapiente voluptatem maxime autem in alias? Reprehenderit
			nisi nam voluptatibus delectus provident praesentium aut.
		</p>
	</div> -->
</div>
