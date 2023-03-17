<script>
	import Video from './lib/Video.svelte'
	import Info from './lib/Info.svelte'
	import './app.css'
	let controller = new ScrollMagic.Controller()

	let sources = [
		'https://www.nma.gov.au/defining-moments/resources/gold-rushes',
		'https://www.nma.gov.au/learn/kspace/victorian-goldfields-1854/kids',
		'https://commons.wikimedia.org/wiki/File:An_Australian_Gold_Diggings.jpg',
	]
</script>

<main class="bg-black text-white">
	<Video bind:controller />
	<!--  -->
	<!-- Q1 -->
	<!--  -->
	<Info bind:controller>
		<div>
			<h1 class="text-4xl font-display">WHAT IS A GOLD RUSH?</h1>
			<p class="text-base max-w-xl">
				A gold rush occurs when there is a new and rapid income of people to a particular area due to newly
				discovered gold. People would flock over to the sites of newly discovered gold to try their luck in
				hopes of making a great fortune, potentially leaving behind their whole family and just going by
				themselves. Finding gold was never guaranteed; miners would head down to the diggings unsure if they
				would make a new fortune or if it would be another day of not finding anything.
			</p>
		</div>
		<div class="relative">
			<div class="absolute -top-5 -right-5 bg-yellow-600 text-white py-1 px-3 rounded-full">
				<h1 class="text-base">
					<a href="#s1">Source 1: 'Prospectors' by ST Gill.</a>
				</h1>
			</div>
			<img
				src="https://www.nma.gov.au/__data/assets/image/0010/547228/MA44137263-prospecting-1200w.jpg"
				alt="Prospectors by ST Gill"
				width="600px"
				height="300px"
			/>
		</div>
	</Info>
	<Info bind:controller>
		<div class="relative">
			<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full">
				<h1 class="text-base">
					<a href="#s2">Source 2: 'Gold Washing' by George French Angas.</a>
				</h1>
			</div>
			<img
				src="https://www.nma.gov.au/__data/assets/image/0007/567070/MA37181365-Gold-washing-1200w.jpg"
				alt="Gold Washing by George French Angas"
				width="600px"
				height="300px"
			/>
		</div>
		<div>
			<h1 class="text-4xl font-display">WHAT IS A GOLD RUSH?</h1>
			<p class="text-base max-w-xl">
				Gold rushes occurred across the world, with major rushes happening in the United States, Australia,
				Canada and South Africa. Multiple thousands of people would head to areas of gold discovery, and up to
				250,000 travelled to the United States for a gold rush, and Australia’s population quadrupled from
				430,000 people to 1.7 million when gold was discovered across the country. The migration of people was
				greatly affected during that time period, with people travelling across the world and settling in the
				areas of gold.
			</p>
		</div>
	</Info>
	<!--  -->
	<!-- Q2 -->
	<!--  -->
	<Info bind:controller>
		<div>
			<h1 class="text-4xl font-display">HOW DID THE BALLARAT GOLD RUSH START?</h1>
			<p class="text-base max-w-xl">
				In August 1851, John Dunlop and James Regan left the gold field at Buninyong when it was overrun with
				many people looking for gold after news got out about the discovery of gold in that region. They moved
				out to Ballarat where they discovered a much richer digging on the 21st of August 1851. However, a
				newspaper reporter had followed them to the diggings and had reported on their finds and, as a result,
				they only had the goldfield to themselves for a week before other prospectors came in. Within a year,
				more than 20,000 diggers were trying their luck in the mine shafts of Ballarat.
			</p>
		</div>
		<div class="relative">
			<div class="absolute -top-5 -right-5 bg-yellow-600 text-white py-1 px-3 rounded-full">
				<h1 class="text-base">
					<a href="#s3">Source 3: 'An Australian Gold Diggings' by Edwin Stockqueler.</a>
				</h1>
			</div>
			<img
				src="https://upload.wikimedia.org/wikipedia/commons/f/ff/An_Australian_Gold_Diggings.jpg"
				alt="An Australian Gold Diggings by Edwin Stockqueler"
				width="600px"
				height="300px"
			/>
		</div>
	</Info>

	<!-- Sources Bibliography -->
	{#each sources as source, i}
		<div id={`s${i + 1}`}>
			{source}
		</div>
	{/each}
</main>
