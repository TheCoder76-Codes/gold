<script>
	import Video from './lib/Video.svelte'
	import Info from './lib/Info.svelte'
	import WorkInProgress from './lib/WorkInProgress.svelte'
	import './app.css'
	let controller = new ScrollMagic.Controller()

	let sources = [
		'https://www.nma.gov.au/defining-moments/resources/gold-rushes',
		'https://www.nma.gov.au/learn/kspace/victorian-goldfields-1854/kids',
		'https://commons.wikimedia.org/wiki/File:An_Australian_Gold_Diggings.jpg',
		'https://museumsvictoria.com.au/media/6928/000010127.jpg',
		'https://museumsvictoria.com.au/media/6933/000010025-loch-ard.jpg',
		'https://museumsvictoria.com.au/media/6931/000017841.jpg',
		'https://museumsvictoria.com.au/media/6936/000009990.jpg',
		'https://collections.museumsvictoria.com.au/items/272753',
	]
</script>

<WorkInProgress />

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
			<div class="absolute -top-5 -right-5 bg-yellow-600 text-white py-1 px-3 rounded-full shadow-md">
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
			<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
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
			<div class="absolute -top-5 -right-5 bg-yellow-600 text-white py-1 px-3 rounded-full shadow-md">
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
	<!--  -->
	<!-- Q3 -->
	<!--  -->
	<Info bind:controller>
		<div>
			<h1 class="text-4xl font-display text-right">WHO CAME TO BALLARAT?</h1>
			<p class="text-base max-w-3xl text-right">
				Many people across the world came to Victoria for the gold rush. Some of the people travelled within
				Australia, from other places to Ballarat for the gold rush. However, most of the prospectors would come
				from places overseas such as Britain, the United States, Germany, and Poland. Australia also saw a large
				influx of Chinese migrants, which was the largest number of non-European settlers to come to Australia
				for the gold rush. Many people abandoned their stable jobs in order to test their luck in the mines, and
				there was a shortage of workers for this reason.
			</p>
		</div>
	</Info>
	<!--  -->
	<!-- Q4 -->
	<!--  -->
	<Info bind:controller>
		<div class="relative">
			<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
				<h1 class="text-base">
					<a href="#s4">Source 4: 1850s Sailing Clipper by Bill Wood.</a>
				</h1>
			</div>
			<img
				src="https://museumsvictoria.com.au/media/6928/000010127.jpg"
				alt="1850s Sailing Clipper by Bill Wood"
				width="500px"
				height="200px"
			/>
		</div>
		<div>
			<h1 class="text-4xl font-display">SHIPS: GETTING TO AUSTRALIA</h1>
			<p class="text-base max-w-xl">
				In the early 1800s, it was common for people to arrive in Australia by sailboat, which would be a long
				and dangerous trip. It would last for around 4 months, however, travelling on a clipper would half this
				time. Later on, auxiliary steamer ships made it possible to travel with both steam and sail, but this
				would be an unlikely trip as steam engines were too inefficient to travel the distance required to get
				to Australia. Despite this, in 1852, the first steamship made its way to Australia. It was mostly
				powered by its steam engine but it was equipped with backup sails as they usually ran out of coal.
				Steamships were usually better as they were made of iron and provided better comfort compared to wooden
				sailboats.
			</p>
		</div>
	</Info>
	<Info bind:controller>
		<div>
			<h1 class="text-4xl font-display">NAVIGATION: GETTING TO AUSTRALIA</h1>
			<p class="text-base max-w-xl">
				Navigating to Australia was a complex and challenging task, requiring great skill from a captain in
				order to arrive safely. Multiple tools were used to get to Australia, including the telescope, marine
				compass, ship’s log, and sextant. To get to Australia, most ships would follow along the ‘Great Circle’
				route as it allowed them to get there faster. They would travel far below the Cape of Good Hope in order
				to enter between 40 and 50 degrees south as it had strong winds getting them towards the direction of
				Australia. However, this route provoked many risks, from drifting icebergs to the wild seas created by
				frequent storms. The slightest of error in navigation along this route could lead to a disaster, and the
				number of deaths increased by taking this route, compared to the traditional way of getting to
				Australia.
			</p>
		</div>
		<div class="relative">
			<div class="absolute -top-5 -right-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
				<h1 class="text-base">
					<a href="#s5">Source 5: The wreck of the 'Loch Ard' in 1878.</a>
				</h1>
			</div>
			<img
				src="https://museumsvictoria.com.au/media/6933/000010025-loch-ard.jpg"
				alt="The wreck of the 'Loch Ard' in 1878"
				width="800px"
				height="600px"
			/>
		</div>
	</Info>
	<Info bind:controller>
		<div class="relative">
			<div class="absolute -top-5 -left-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
				<h1 class="text-base">
					<a href="#s6">Source 6: The 'Great Circle' route used to get to Australia.</a>
				</h1>
			</div>
			<img
				src="https://museumsvictoria.com.au/media/6931/000017841.jpg"
				alt="The 'Great Circle' route used to get to Australia"
				width="900px"
				height="700px"
			/>
		</div>
	</Info>
	<Info bind:controller>
		<div>
			<h1 class="text-4xl font-display">LIFE ON BOARD: GETTING TO AUSTRALIA</h1>
			<p class="text-base max-w-3xl">
				Most people making their way to Australia were not familiar with sea travel, and the travel to Australia
				involved navigating through some of the wildest oceans. Usually, passengers would travel in steerage
				class, which were cramped quarters below sea level supporting the spread of disease and sickness, making
				an unpleasant journey. Seasickness was common, especially among those who were unaccustomed to sea
				travel. As a result of this, death at sea was very common, with 1 in 5 children and 1 in 60 adults not
				being able to survive the journey.
			</p>
			<p class="text-base max-w-3xl mt-3">
				Water was kept in barrels, but they were left open where algae would grow and rats and mice would fall
				in making the water stale after just a few months. Food was kept in barrels that were opened when needed
				by the cooks, which were usually fitted with lids. However, the cooks would often leave the lids of the
				barrels overnight letting in rats and mice to raid the storage. Hygiene was no better, with most ships
				only providing basic toilet and cleaning facilities, but most passengers just used the upper decks as
				open-air toilets. The waste from toilets was stored in the bottom of the ship, creating a worse
				experience for people in steerage. Simple practices of hygiene were unknown at the time, and outbreaks
				of multiple diseases happened frequently on ships.
			</p>
		</div>
	</Info>
	<Info bind:controller>
		<div class="relative">
			<div class="absolute -top-5 -right-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
				<h1 class="text-base">
					<a href="#s7">Source 7: 'Emigrants at dinner' by unknown artist.</a>
				</h1>
			</div>
			<img
				src="https://museumsvictoria.com.au/media/6936/000009990.jpg"
				alt="'Emigrants at dinner' by unknown artist"
				width="800px"
				height="600px"
			/>
		</div>
	</Info>
	<Info bind:controller>
		<div>
			<h1 class="text-4xl font-display">EXPERIENCE: GETTING TO AUSTRALIA</h1>
			<p class="text-base max-w-xl">
				Ally Heathcote was a passenger from England to Melbourne on the ‘SS Northumberland’. Heathcote
				experienced a “storm” upon her journey to Australia, where she was “wondering how long [it] would last”
				wanting “protection when crash went something on deck”. Water came in “over the decks and down into the
				cabin[s]”, and people would “rush out of their cabins looking terrified” as they flooded in second
				class. A few days earlier, she “starved to death almost” as their “ships rolls [them] about … every meal
				time”. They had to “hold on to the tables and seats and keep [their] cups from wandering all over the
				cabin” as the seas were so violent. During the night, they were “constantly on the move, first one side
				[of the bed] then the other”, however, they “fared better than the second cabin passengers, as they have
				the engine right in the midst of them” making for a hot and noisy journey. Heathcote demonstrates an
				example of life on board, and the horrible conditions those experienced travelling to Australia.
			</p>
		</div>
		<div class="relative">
			<div class="absolute -top-5 -right-5 bg-amber-500 text-white py-1 px-3 rounded-full shadow-md">
				<h1 class="text-base">
					<a href="#s8">Source 8: Ally Heathcote's diary.</a>
				</h1>
			</div>
			<img
				src="https://collections.museumsvictoria.com.au/content/media/32/296632-small.jpg"
				alt="The wreck of the 'Loch Ard' in 1878"
				width="500px"
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
